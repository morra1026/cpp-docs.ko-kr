---
title: Boxed 값에 대 한 추적 핸들 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- boxed value types, tracking handle to
ms.assetid: 16c92048-5b74-47d5-8eca-dfea3d38879a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: c7e26efae93b509700c3bb0c992d9f397559e99f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46380732"
---
# <a name="a-tracking-handle-to-a-boxed-value"></a>boxed 값에 대한 추적 핸들

참조 값 형식에 대 한 추적 핸들 사용 Visual c + + Managed Extensions for c + + 변경 되었습니다.

Boxing은 통합 된 CLR 형식 시스템의 평범 합니다. 값 형식 상태로 참조 유형은 암시적 쌍을 하는 동안 직접 포함 되어: 관리 되는 힙에 할당 된 명명 되지 않은 개체에 대 한 핸들입니다. 초기화 또는 값 형식 할당을 `Object`, 예를 들어 필요-이 이미지의 발생 위치-CLR 힙에 값 형식을 배치 하는 것 먼저 연결된 된 메모리를 할당 하 여 다음 값 형식의 상태를 복사 하 여 그런 다음이 익명 값/참조 하이브리드의 주소를 반환 합니다. 따라서 코드가 C#

```cpp
object o = 1024; // C# implicit boxing
```

코드를 단순화 하 여 명백한 이루어집니다 보다에서 많은 이점을 진행 있습니다. C#의 디자인 내부적으로 수행 된 작업의 뿐만 아니라 하지만 자체 boxing 추상화의 복잡성을 숨깁니다. Managed Extensions 반면, c + +에 대 한 관련된 효율성에 대해 잘못 된 시키는이, 명시적 명령 요구 하 여 사용자의 얼굴에 넣습니다.

```cpp
Object *o = __box( 1024 ); // Managed Extensions explicit boxing
```

Visual c + +에서 암시적 boxing이 같습니다.

```cpp
Object ^o = 1024; // new syntax implicit boxing
```

`__box` 키워드 없는 Managed Extensions 내에서 중요 한 서비스는 C# 및 Visual Basic과 같은 언어에서 의도적인: 어휘 및 추적 관리 되는 힙에서 boxed 인스턴스를 직접 조작 하는 것에 대 한 처리를 제공 합니다. 예를 들어, 다음 작은 프로그램을 고려 합니다.

```cpp
int main() {
   double result = 3.14159;
   __box double * br = __box( result );

   result = 2.7;
   *br = 2.17;
   Object * o = br;

   Console::WriteLine( S"result :: {0}", result.ToString() ) ;
   Console::WriteLine( S"result :: {0}", __box(result) ) ;
   Console::WriteLine( S"result :: {0}", br );
}
```

세 가지 호출에 대해 생성 된 기본 코드 `WriteLine` boxed 값의 값에 액세스 하는 다양 한 비용 (덕분 치러야 하기 이러한 차이점을 지적 하는 것에 대 한), 입력이 지정 된 줄에서 각 연관 된 오버 헤드를 표시 하는 위치 표시 호출 합니다.

```cpp
// Console::WriteLine( S"result :: {0}", result.ToString() ) ;
ldstr      "result :: {0}"
ldloca.s   result  // ToString overhead
call       instance string  [mscorlib]System.Double::ToString()  // ToString overhead
call       void [mscorlib]System.Console::WriteLine(string, object)

// Console::WriteLine( S"result :: {0}", __box(result) ) ;
Ldstr    " result :: {0}"
ldloc.0
box    [mscorlib]System.Double // box overhead
call    void [mscorlib]System.Console::WriteLine(string, object)

// Console::WriteLine( S"result :: {0}", br );
ldstr    "result :: {0}"
ldloc.0
call     void [mscorlib]System.Console::WriteLine(string, object)
```

Boxed 값 형식에 직접 전달 `Console::WriteLine` boxing와 호출할 필요가 제거 `ToString()`합니다. (물론는 초기화를 이전 boxing `br`이므로 실제로 사용 하지 않으면 어떠한 이점도 없습니다 `br` 작동 하도록 합니다.

새 구문, boxed 값 형식에 대 한 지원은 훨씬 더 세련 되 고 통합 형식 시스템 내에서 그대로 유지 하면서 기능입니다. 예를 들어, 다음은 위의 작은 프로그램의 번역이입니다.

```cpp
int main()
{
   double result = 3.14159;
   double^ br = result;
   result = 2.7;
   *br = 2.17;
   Object^ o = br;
   Console::WriteLine( "result :: {0}", result.ToString() );
   Console::WriteLine( "result :: {0}", result );
   Console::WriteLine( "result :: {0}", br );
}
```

## <a name="see-also"></a>참고 항목

[값 형식 및 동작(C++/CLI)](../dotnet/value-types-and-their-behaviors-cpp-cli.md)<br/>
[방법: 명시적으로 boxing 요청](../dotnet/how-to-explicitly-request-boxing.md)