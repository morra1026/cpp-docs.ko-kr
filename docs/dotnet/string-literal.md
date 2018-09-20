---
title: 문자열 리터럴 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- string literals
- strings [C++], string literals
ms.assetid: 6d1fc3f8-0d58-4d68-9678-16b4f6dc4766
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 41f1996cd4f4caf24ac08d09b05e636cb09f7eed
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46415267"
---
# <a name="string-literal"></a>문자열 리터럴

문자열 리터럴의 처리 Visual c + + Managed Extensions for c + + 변경 되었습니다.

Managed Extensions for c + + 언어 디자인, 관리 되는 문자열 리터럴을 사용 하 여 리터럴 문자열을 앞에서 표시 된는 `S`합니다. 예를 들어:

```
String *ps1 = "hello";
String *ps2 = S"goodbye";
```

두 초기화 사이의 오버 헤드가 성능 trivial이 아닌 것으로 밝혀졌습니다, 다음 CIL로 표현에서는 통해 볼 수 있듯이 **ildasm**:

```
// String *ps1 = "hello";
ldsflda    valuetype $ArrayType$0xd61117dd
     modopt([Microsoft.VisualC]Microsoft.VisualC.IsConstModifier)
     '?A0xbdde7aca.unnamed-global-0'

newobj instance void [mscorlib]System.String::.ctor(int8*)
stloc.0

// String *ps2 = S"goodbye";
ldstr      "goodbye"
stloc.0
```

에 기억 (학습) 리터럴 문자열을 접두사로 주목할 만한 절약을 사용 하 여 이것이 `S`합니다. 새 구문에서는 문자열 리터럴의 처리 투명 하 게, 사용 컨텍스트에 의해 결정 합니다. `S` 더 이상 지정 해야 합니다.

어떤 점이 있는 해야 명시적으로 하는 경우 컴파일러가 하도록 특정 해석을? 이러한 경우에 명시적 캐스트를 적용합니다. 예를 들어:

```
f( safe_cast<String^>("ABC") );
```

또한 리터럴 문자열은 이제는 `String` 표준 변환 대신 간단한 변환 합니다. 들릴 수도 없습니다 포함 하는 오버 로드 된 함수 집합의 해상도 변경 하기는 훨씬 등을 `String` 및 `const char*` 경쟁 정식 매개 변수로 합니다. 이전에 해상도 `const char*` 인스턴스 모호한 것으로 플래그가 지정 이제 됩니다. 예를 들어:

```
ref struct R {
   void f(const char*);
   void f(String^);
};

int main () {
   R r;
   // old syntax: f( const char* );
   // new syntax: error: ambiguous
   r.f("ABC"); 
}
```

차이가 있는 이유는 무엇입니까? 명명 된 인스턴스가 둘 이상 이후 `f` 존재 호출에 적용 될 함수 오버 로드 확인 알고리즘이 프로그램에서 필요 합니다. 정식 함수를 오버 로드 확인에는 세 가지 단계가 포함 됩니다.

1. 후보 함수의 컬렉션입니다. 후보 함수 어휘 적으로 호출할 함수의 이름을 일치 하는 범위 내에서 이러한 메서드는 합니다. 예를 들어, 이후 `f()` 의 인스턴스를 통해 호출 됩니다 `R`모든 명명 된 함수 `f` 의 멤버가 아닌 `R` (또는 해당 기본 클래스 계층 구조) 후보 함수 없는 합니다. 예제에서는 두 후보 함수가 있습니다. 두 멤버 함수는 이러한 `R` 라는 `f`합니다. 후보 함수 집합이 비어 있으면이 단계는 호출이 실패 합니다.

1. 후보 함수 중에서 사용 가능한 함수 집합입니다. 실행 가능한 함수 호출에서 인수 및 해당 형식에 따라 지정 된 인수를 사용 하 여 호출할 수 있는 하나입니다. 예제에서는 두 후보 함수에도 가능한 함수. 사용 가능한 함수 집합이 비어 있으면이 단계는 호출이 실패 합니다.

1. 가장 일치 하는 호출을 나타내는 함수를 선택 합니다. 실행 가능한 함수 매개 변수의 형식에 대 한 인수를 변환할 적용 되는 변환을 순위 하면 됩니다. 이 비교적 간단 단일 매개 변수 함수를 사용 하 여 여러 매개 변수가 있는 경우 다소 복잡 한 됩니다. 가장 일치 하는 경우이 단계는 호출이 실패 합니다. 즉, 정식 매개 변수 형식의 실제 인수의 형식을 변환 하는 데 필요한 변환을 동등 경우. 호출이 모호한 것으로 플래그가 지정 됩니다.

Managed extensions에서이 호출의 해상도 `const char*` 가장 일치 하는 인스턴스로. 새 구문에서 일치 하는 데 필요한 변환 `"abc"` 하 `const char*` 및 `String^` 동일 이제-즉, 동등-이므로 호출으로 플래그가 지정 되어 잘못 된-즉, 모호한 것으로 합니다.

이 두 질문에 대 한 안내 합니다.

- 실제 인수의 유형을 `"abc"`?

- 형식 변환 보다 다른 경우를 결정 하는 데는 알고리즘은 무엇입니까?

문자열 리터럴의 형식 `"abc"` 는 `const char[4]` -리터럴 모든 문자열의 끝에는 암시적 null 종결 문자는 합니다.

형식 변환 가능한 형식 변환 계층에 배치 하는 것 다른 것 보다 더 나은 경우 결정 하기 위한 알고리즘입니다. 다음 알고는 해당 계층의 모든이 변환은 물론은 암시적입니다. 계층 방식과 유사 하 게 재정의 명시적 캐스트 표기법을 사용 하 여 괄호 식의 일반적인 연산자 우선 순위를 재정의 합니다.

1. 정확 하 게 일치 하는 것이 좋습니다. 놀랍게도 정확 하 게 일치 하는 인수에 대 한 것을 하지 않아도; 매개 변수 형식과 정확히 일치 가까이 되도록 해야 합니다. 어떤 일이 일어나는지이 예 및 언어 어떻게 변경 되었는지 이해 하는 키입니다.

1. 홍보 행사 표준 변환 보다 좋습니다. 예를 들어, 승격을 `short int` 에 `int` 변환 보다 나은 `int` 에 `double`.

1. 표준 변환을 boxing 변환 보다 좋습니다. 예를 들어, 변환는 `int` 에 `double` 는 보다 잘 boxing는 `int` 에 `Object`.

1. boxing 변환이 암시적 사용자 정의 변환을 보다 좋습니다. 예를 들어, boxing을 `int` 에 `Object` 의 변환 연산자를 적용 하는 보다 나은 `SmallInt` 값 클래스.

1. 암시적 사용자 정의 변환을 전혀 없는 변환 보다 더 나은있지 않습니다. 암시적 사용자 정의 변환이 (매개 변수 배열 또는 해당 위치에 있는 줄임표를 형식 서명을 포함 될 수 있습니다 주의)와 오류에 앞서 마지막 종료 됩니다.

따라서 어떤 의미를 정확 하 게 일치는 반드시 정확 하 게 일치 하는 항목이 없습니다. 예를 들어 `const char[4]` 정확히 일치 하지 않는 하나 `const char*` 또는 `String^`, 모호성 예제는 두 명의 충돌 하는 정확한 일치 항목이 아직!

정확히 일치 되는 경우가 다양 한 trivial 변환만 포함 합니다. ISO-c + +에서 적용할 수 있습니다 하 고, 정확한 일치로 한정할 수는 4 개의 trivial 변환이 있습니다. 세 가지 lvalue 변환 이라고 합니다. 네 번째 형식 한정 변환을 이라고 합니다. 세 가지 lvalue 변환 한정 변환이 필요로 하나 보다 더 정확한 일치로 처리 됩니다.

한 가지 형태의 lvalue 변환은 포인터를 네이티브 배열 변환입니다. 이 일치 하는 관련 정보를 `const char[4]` 에 `const char*`합니다. 따라서 일치 `f("abc")` 에 `f(const char*)` 정확 하 게 일치 합니다. 언어는 이전 버전에서이 최상의 일치 사실입니다.

컴파일러에 모호한 경우로 호출을 플래그에 대 한 필요는 변환을 `const char[4]` 에 `String^` 수도 정확히 일치 하는 간단한 변환을 통해. 이 변경 내용을 새 언어 버전에 도입 되었습니다. 이 때문에 호출이 플래그가 지정 모호한 것으로 하며

## <a name="see-also"></a>참고 항목

[일반적인 언어 변경 사항(C++/CLI)](../dotnet/general-language-changes-cpp-cli.md)<br/>
[String](../windows/string-cpp-component-extensions.md)