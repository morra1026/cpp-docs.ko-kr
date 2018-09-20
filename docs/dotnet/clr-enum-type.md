---
title: CLR 열거형 형식 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- scope, of CLR enum
- enum struct keyword [C++]
- enum class keyword [C++]
ms.assetid: 4541d952-97bb-4e35-a7f8-d14f5f6a6606
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: a39c451bcff7b5b3b1d7dd9f0d3925616b9d6aab
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46436229"
---
# <a name="clr-enum-type"></a>CLR 열거형 형식

선언 및 열거형의 동작에서에서 변경 되었습니다 Managed Extensions for c + + Visual c + +.

Managed Extensions 열거형 선언 앞에 `__value` 키워드입니다. 네이티브 열거형에서 파생 되는 CLR 열거형 구분 하기 위해 여기서는 `System::ValueType`, 유사한 기능을 제안 하는 동안. 예를 들어:

```
__value enum e1 { fail, pass };
public __value enum e2 : unsigned short  {
   not_ok = 1024,
   maybe, ok = 2048
};
```

새 구문 보다의 값 형식 루트의 클래스 특성을 강조 하 여 네이티브를 구분 하는 문제 및 CLR 열거형을 해결 합니다. 따라서 합니다 `__value` 공백이 포함 된 키워드 쌍을 사용 하 여 대체 키워드 무시 되 `enum class`합니다. 이 제공 참조, 값 및 인터페이스 클래스의 선언에 쌍을 이루는 키워드 대칭성을 확립을 합니다.

```
enum class ec;
value class vc;
ref class rc;
interface class ic;
```

열거형 쌍의 번역 `e1` 고 `e2` 새 구문에서 형식은 다음과 같습니다.

```
enum class e1 { fail, pass };
public enum class e2 : unsigned short {
   not_ok = 1024,
   maybe, ok = 2048
};
```

이 작은 구문 변경 외에도 CLR 열거형 형식의 동작을 여러 가지 방법으로에서 변경 되었습니다.

- CLR 열거형의 정방향 선언 더 이상 지원 되지. 매핑은 없습니다. 컴파일 타임 오류로 플래그가 지정 하기만 하면 됩니다.

```
__value enum status; // Managed Extensions: ok
enum class status;   // new syntax: error
```

- 기본 제공 산술 형식 간의 오버 로드 확인 및 `Object` 클래스 계층 구조를 두 언어 버전 간에 바뀌었습니다! 부작용으로 CLR 열거형 산술 형식으로 더 이상 암시적으로 변환 됩니다.

- 새 구문에서 CLR 열거형에는 Managed extensions에서에 해당 되지 않는 자체 범위를 유지 관리 합니다. 이전에 열거자를 포함 하는 열거형의 범위 내에 표시 되었습니다. 이제 열거자가 열거형의 범위 내에서 캡슐화 됩니다.

## <a name="clr-enums-are-a-kind-of-object"></a>CLR 열거형은 일종의 개체를

다음과 같은 코드 조각을 생각해 봅시다.

```
__value enum status { fail, pass };

void f( Object* ){ Console::WriteLine("f(Object)\n"); }
void f( int ){ Console::WriteLine("f(int)\n"); }

int main()
{
   status rslt = fail;

   f( rslt ); // which f is invoked?
}
```

네이티브 c + + 프로그래머가 대 한 자연 인스턴스의 오버 로드 된 질문에 답변 `f()` 가 호출의 임을 `f(int)`합니다. 열거형 기호 정수 계열 상수 이며이 경우 보다 우선적으로 적용 되는 표준 정수 계열 확장에 참여 합니다.  했는데 사실 Managed Extensions에서이 호출을 확인 하는 인스턴스. 에서는 사용 하는 네이티브 c + + 사고-에서 문제가 없지만 기존 BCL (기본 클래스 라이브러리) 프레임 워크를 사용 하 여 상호 작용할 때가 아니라 여러 가지 문제가-발생이 위치는 `Enum` 클래스에서 직접 파생 됩니다 하지 `Object`합니다. Visual c + + 언어 디자인에서는 인스턴스의 `f()` 호출의 됩니다 `f(Object^)`합니다.

CLR 열거형 형식 산술 형식 사이의 암시적 변환을 지원 하지 방식은 Visual c + +는이 적용 하도록 선택 했습니다. 즉, 산술 형식으로 CLR 열거형 형식 개체의 모든 할당이 명시적 캐스트를 필요 합니다. 따라서 예를 들어

```
void f( int );
```

Managed extensions를 호출 하는 오버 로드 되지 않은 방법으로

```
f( rslt ); // ok: Managed Extensions; error: new syntax
```

확인을 포함 하는 값은 `rslt` 정수 값으로 암시적으로 변환 됩니다. Visual c + +에서는이 호출에는 컴파일이 실패 합니다. 올바르게 변환, 변환 연산자를 삽입 해야 합니다.

```
f( safe_cast<int>( rslt )); // ok: new syntax
```

## <a name="the-scope-of-the-clr-enum-type"></a>CLR 열거형 형식 범위

C 및 c + + 언어 간의 변경 사항 중 하나에 c + +에서 구조체 시설 내의 범위를 추가 했습니다. C에서 구조체는 인터페이스 또는 관련된 범위를 지원 하지 않는 집계 데이터 뿐입니다. 시간에 상당히 근본적인 변경 되었으며 C 언어에서 제공 하는 많은 새 c + + 사용자에 대 한 경합이 많은 문제가 있습니다. 네이티브 및 CLR 열거형 간의 관계는 유사 합니다.

Managed extensions에서는 하려고 없을 경우 네이티브 열거형에서 범위를 시뮬레이션 하기 위해 CLR 열거형의 열거자에 대 한 약하게 삽입 된 이름을 정의 합니다. 이 성공적인 증명 하지 않았습니다. 그러면 경우 열거자 이름 충돌을 관리 하기 어려운 생성, 전역 네임 스페이스에는 문제가입니다. 새 구문에서 호환성을 유지할 수 다른 CLR 언어로 CLR 열거형에서 범위를 지원 합니다.

즉, CLR 열거형의 열거자의 정규화 되지 않은 사용 새 구문으로 인식 되지 않습니다. 실제 예제를 살펴보겠습니다.

```
// Managed Extensions supporting weak injection
__gc class XDCMake {
public:
   __value enum _recognizerEnum {
      UNDEFINED,
      OPTION_USAGE,
      XDC0001_ERR_PATH_DOES_NOT_EXIST = 1,
      XDC0002_ERR_CANNOT_WRITE_TO = 2,
      XDC0003_ERR_INCLUDE_TAGS_NOT_SUPPORTED = 3,
      XDC0004_WRN_XML_LOAD_FAILURE = 4,
      XDC0006_WRN_NONEXISTENT_FILES = 6,
   };

   ListDictionary* optionList;
   ListDictionary* itagList;

   XDCMake() {
      optionList = new ListDictionary;

      // here are the problems...
      optionList->Add(S"?", __box(OPTION_USAGE)); // (1)
      optionList->Add(S"help", __box(OPTION_USAGE)); // (2)

      itagList = new ListDictionary;
      itagList->Add(S"returns",
         __box(XDC0004_WRN_XML_LOAD_FAILURE)); // (3)
   }
};
```

정규화 되지 않은 세 개의 각 열거자 이름 사용 (`(1)`, `(2)`, 및 `(3)`) 컴파일할 소스 코드에 대 한 순서 대로 새 구문으로 변환할 정규화 해야 합니다. 다음은 원래 소스 코드를 올바르게 변환이입니다.

```
ref class XDCMake {
public:
   enum class _recognizerEnum {
      UNDEFINED, OPTION_USAGE,
      XDC0001_ERR_PATH_DOES_NOT_EXIST = 1,
      XDC0002_ERR_CANNOT_WRITE_TO = 2,
      XDC0003_ERR_INCLUDE_TAGS_NOT_SUPPORTED = 3,
      XDC0004_WRN_XML_LOAD_FAILURE = 4,
      XDC0006_WRN_NONEXISTENT_FILES = 6
   };

   ListDictionary^ optionList;
   ListDictionary^ itagList;

   XDCMake() {
      optionList = gcnew ListDictionary;
      optionList->Add("?",_recognizerEnum::OPTION_USAGE); // (1)
      optionList->Add("help",_recognizerEnum::OPTION_USAGE); //(2)
      itagList = gcnew ListDictionary;
      itagList->Add( "returns",
         _recognizerEnum::XDC0004_WRN_XML_LOAD_FAILURE); //(3)
   }
};
```

이 네이티브 CLR 열거형 사이 디자인 전략을 변경합니다. Visual c + +에서 관련된 범위를 유지 하는 CLR 열거형에 비효율적일 클래스 내에서 열거형 선언을 캡슐화 하는 것이 것입니다. 이 관용구 발전 cfront 2.0 Bell laboratories의 시간대에 전역 이름 오염 문제를 해결 하기 위해.

Jerry Schwarz Bell laboratories에서 새 iostream 라이브러리의 원래 베타 릴리스에서 캡슐화 하지 않았으므로 라이브러리와 같은 일반적인 열거자에 대해 정의 된 모든 연결된 열거형 `read`, `write`, `append`등 를 수행 하 여 기존 코드를 컴파일하는 데 사용자가 거의 불가능 합니다. 같은 이름, 복잡 하 게 만드는 한 가지 해결 되었을 `io_read`, `io_write`등입니다. 열거형에서 범위를 추가 하 여 언어를 수정 하려면 두 번째 해결 되었을 했지만이 적고 시. 중간 솔루션을 캡슐화 클래스 내에서 열거형 또는 클래스 계층 구조에서 태그 이름과 열거형의 열거자는 바깥쪽 클래스 범위를 채웁니다.) 열거형 클래스 내에서 원래 이상 배치에 대 한 동기 철학적, 없습니다, 있지만 전역 네임 스페이스 공해 문제에 대 한 실용적인 응답 합니다.

Visual c + + 열거형을 사용 하 여 더 이상 없기는 enum 클래스 내에서 캡슐화로 운 점이 합니다. 사실 보면는 `System` 네임 스페이스를 보면 해당 열거형, 클래스 및 인터페이스가 모두 동일한 선언 공간 범위입니다.

## <a name="see-also"></a>참고 항목

[값 형식 및 동작(C++/CLI)](../dotnet/value-types-and-their-behaviors-cpp-cli.md)<br/>
[enum 클래스](../windows/enum-class-cpp-component-extensions.md)