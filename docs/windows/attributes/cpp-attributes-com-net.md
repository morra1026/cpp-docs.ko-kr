﻿---
title: COM 및.NET에 대한 C++ 특성
ms.custom: index-page
ms.date: 11/19/2018
ms.topic: conceptual
helpviewer_keywords:
- attributes [C++/CLI], reference topics
ms.assetid: 613a3611-b3eb-4347-aa38-99b654600e1c
ms.openlocfilehash: f9d339860e9d2bdb8d66f6b7f8f49d3993b2d5cf
ms.sourcegitcommit: 8105b7003b89b73b4359644ff4281e1595352dda
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57820743"
---
# <a name="c-attributes-for-com-and-net"></a>COM 및.NET에 대한 C++ 특성

Microsoft은.NET Framework 공용 언어 런타임 개발 및 COM 프로그래밍을 단순화 하는 C++ 특성 집합을 정의 합니다. 소스 파일에서 특성을 포함 하는 경우 컴파일러는 공급자 코드를 삽입 하거나 생성 된 개체 파일의 코드를 수정 하는 Dll 사용 하 여 작동 합니다. 이러한 특성은.idl 파일, 인터페이스, 형식 라이브러리 및 다른 COM 요소 생성에 도움이 됩니다. 통합된 개발 환경 (IDE), 마법사 및 속성 창에서 특성은 지원 됩니다.

배경이 해야 특성 COM 개체를 작성 하는 데 필요한 자세한 코딩의 일부를 제거 하는 동안 [COM 기본 사항](/windows/desktop/com/the-component-object-model) 가장 사용 합니다.

> [!NOTE]
> C++ 표준 특성 찾고자 하는 경우 참조 [특성](../../cpp/attributes.md)합니다.

## <a name="purpose-of-attributes"></a>특성의 용도

언어의 기본 구조를 중단 하지 않고 현재 불가능 방향으로 C++를 확장 하는 특성입니다. 특성을 통해 공급자 (별도 Dll) 언어 기능을 동적으로 확장 합니다. 특성의 기본 목적은 구성 요소 개발자의 생산성 수준을 증가 하는 것 외에도 COM 구성 요소 작성을 간소화 하기 위해. 특성을 적용할 수 클래스, 데이터 멤버, 멤버 함수 등 거의 모든 C++ 구문에 있습니다. 다음은이 새 기술을 통해 제공 되는 혜택을 강조 표시 합니다.

- 친숙하고 간단한 호출 규칙을 표시합니다.

- 매크로와는 달리 디버거에서 인식하는 삽입 코드를 사용합니다.

- 세부적인 구현이 필요하지 않은, 기본 클래스에서 쉽게 파생하는 것을 허용합니다.

- 몇 가지 간단한 특성을 사용 하 여 COM 구성 요소에서 필요한 IDL 코드의 양이 대체 합니다.

예를 들어 제네릭 ATL 클래스에 대 한 간단한 이벤트 싱크를 구현 하려면 적용할 수 있습니다 합니다 [event_receiver](event-receiver.md) 와 같은 특정 클래스에 특성 `CMyReceiver`합니다. `event_receiver` 특성은 개체 파일에 적절 한 코드를 삽입 하는 Visual C++ 컴파일러에 의해 컴파일됩니다.

```cpp
[event_receiver(com)]
class CMyReceiver
{
   void handler1(int i) { ... }
   void handler2(int i, float j) { ... }
}
```

`CMyReceiver` 메서드 `handler1` 및 `handler2`를 설정하여 이벤트를 처리할 수 있으며(내장 함수 [__hook](../../cpp/hook.md)를 사용), 이는 [event_source](event-source.md)를 사용하여 생성할 수 있습니다.

## <a name="basic-mechanics-of-attributes"></a>특성의 기본 메커니즘

프로젝트에 특성을 삽입 하는 방법은 세 가지가 있습니다. 첫째, 삽입할 수 있습니다 이러한 수동으로 소스 코드입니다. 둘째,이 프로젝트에서 개체의 속성 표를 사용 하 여 삽입할 수 있습니다. 마지막으로, 다양 한 마법사를 사용 하 여 삽입할 수 있습니다. 사용 하 여 대 한 자세한 내용은 합니다 **속성** 창 및 다양 한 마법사를 참조 하십시오 [Creating and Managing Visual C++ Projects](../../build/creating-and-managing-visual-cpp-projects.md)합니다.

로 이전에 프로젝트를 빌드할 때 컴파일러 구문 분석 각 C++ 소스 파일을 개체 파일을 생성 합니다. 그러나 컴파일러는 특성을 발견 하면 해당 구문 분석 되 고 구문적으로 확인 합니다. 컴파일러가 다음 동적으로 공급자를 호출할 특성 코드를 삽입 하거나 컴파일 타임에 기타 수정 작업을 확인 합니다. 공급자 구현 형식 특성에 따라 다릅니다. 예를 들어, ATL 관련 특성 Atlprov.dll 여 구현 됩니다.

다음 그림에서는 컴파일러 및 특성 공급자 간의 관계를 보여 줍니다.

![구성 요소 특성 통신](../media/vccompattrcomm.gif "구성 요소 특성 통신")

> [!NOTE]
> 특성 사용 소스 파일의 내용을 변경 하지 않습니다. 디버깅 세션 중에 생성 된 특성 코드를 표시 됩니다. 또한 프로젝트의 각 소스 파일에 대 한 특성 대체의 결과 표시 하는 텍스트 파일을 생성할 수 있습니다. 이 절차에 대 한 자세한 내용은 참조 하세요. [/Fx (삽입 된 코드 병합)](../../build/reference/fx-merge-injected-code.md) 하 고 [삽입 된 코드 디버그](/visualstudio/debugger/how-to-debug-injected-code)합니다.

대부분의 C++ 구문에 같은 특성에는 적절 한 용도 정의 하는 특성 집합입니다. 이 특성의 컨텍스트로 라고 하 고는 각 특성 참조 항목에 대한 특성 상황에 맞는 테이블에서 처리 됩니다. 예를 들어 합니다 [coclass](coclass.md) 특성 수와 반대로 기존 클래스 또는 구조체에 적용 하는 수는 [cpp_quote](cpp-quote.md) 특성을 C++ 소스 파일 내의 아무 곳 이나 삽입할 수 있습니다.

## <a name="building-an-attributed-program"></a>특성을 사용하는 프로그램 빌드

소스 코드를 Visual C++ 특성을 추가한 후를 형식 라이브러리 및.idl 파일을 생성 하기 위해 Visual C++ 컴파일러를 확인할 수 있습니다. 다음 링커 옵션.tlb 및.idl 파일을 빌드할 수 있습니다.

- [/IDLOUT](../../build/reference/idlout-name-midl-output-files.md)

- [/IGNOREIDL](../../build/reference/ignoreidl-don-t-process-attributes-into-midl.md)

- [/MIDL](../../build/reference/midl-specify-midl-command-line-options.md)

- [/TLBOUT](../../build/reference/tlbout-name-dot-tlb-file.md)

일부 프로젝트는 여러 독립적인.idl 파일을 포함합니다. 이러한 두 개 이상의.tlb 파일을 생성 하 고 필요에 따라 리소스 블록에 바인딩하고에 사용 됩니다. 이 시나리오는 Visual C++에서 현재 지원 되지 않습니다.

또한 Visual C++ 링커는 모든 IDL 관련 특성 정보를 단일 MIDL 파일로 출력 합니다. 단일 프로젝트에서 두 개의 형식 라이브러리를 생성할 수 없음이 됩니다.

## <a name="contexts"></a> 특성 컨텍스트

네 가지 기본 필드를 사용하여 C++ 특성을 설명할 수 있습니다: 대상에 적용 될 수 있습니다 (**적용 대상**) 여부 반복 하는 경우 (**Repeatable**), 필요한 다른 특성이 ( **필수 특성**), 및 기타 특성을 사용 하 여 호환성 문제 (**잘못 된 특성이**). 이러한 필드는 각 특성의 참조 항목에서 해당 테이블에 나열 됩니다. 이러한 각 필드는 아래 설명 되어 있습니다.

### <a name="applies-to"></a>적용 대상

이 필드는 지정된 된 특성에 대 한 법적 대상이 여러 C++ 언어 요소를 설명 합니다. 예를 들어 특성에서 "class"를 지정 하는 경우는 **적용 대상** 필드 나타냅니다 특성을 법적 C++ 클래스에만 적용 될 수 있습니다. 특성 클래스의 멤버 함수에 적용 되는 경우 구문 오류를 초래 합니다.

자세한 내용은 [용도별 특성](attributes-by-usage.md)합니다.

### <a name="repeatable"></a>반복 가능

이 필드는 동일한 대상에 특성을 반복적으로 적용할 수 있는지 여부를 알려 줍니다. 대부분의 특성 재현이 불가능 합니다.

### <a name="required-attributes"></a>필수 특성

이 필드는 지정된 특성이 제대로 작동하기 위해 존재해야 하는(즉, 동일한 대상에 적용되는) 다른 특성을 나열합니다. 특성에 이 필드에 대한 항목이 있는 것은 드뭅니다.

### <a name="invalid-attributes"></a>잘못 된 특성

이 필드는 지정된 된 특성을 사용 하 여 호환 되지 않는 다른 특성을 나열 합니다. 특성에 이 필드에 대한 항목이 있는 것은 드뭅니다.

## <a name="in-this-section"></a>섹션 내용

[특성 프로그래밍 FAQ](attribute-programming-faq.md)<br/>
[그룹별 특성](attributes-by-group.md)<br/>
[용도별 특성](attributes-by-usage.md)<br/>
[특성 사전순 참조](attributes-alphabetical-reference.md)
