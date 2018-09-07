---
title: Boxing (C + + /cli CX) | Microsoft Docs
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: language-reference
ms.assetid: edfb12fa-2a9b-42f6-bdac-d4d76cb8274e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7e9ab84bf840f01fbb22ef3b2510056338d10c74
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44108386"
---
# <a name="boxing-ccx"></a>Boxing(C++/CX)

*Boxing* 와 같은 값 형식 변수 래핑하 [Windows::Foundation::DateTime](https://msdn.microsoft.com/library/windows/apps/windows.foundation.datetime.aspx)-또는와 같은 기본 스칼라 형식이 `int`-ref 클래스 변수를 사용 하는 메서드에 전달 되 면에서 [ Platform:: object ^](../cppcx/platform-object-class.md) 입력된 형식으로 합니다.

## <a name="passing-a-value-type-to-an-object-parameter"></a>Object^ 매개 변수에 값 형식 전달

[Platform::Object^](../cppcx/platform-object-class.md)형식의 메서드 매개 변수에 전달하기 위해 명시적으로 변수를 boxing할 필요는 없지만 이전에 boxing된 값을 검색할 때는 명시적으로 원래 형식으로 캐스팅해야 합니다.

[!code-cpp[cx_boxing#01](../cppcx/codesnippet/CPP/cx_boxing/class1.cpp#01)]

### <a name="using-platformiboxt-to-support-nullable-value-types"></a>Platform:: ibox를 사용 하 여\<T > nullable 값 형식을 지원 하기 위해

C# 및 Visual Basic에서는 null 허용 값 형식의 개념을 지원합니다. C + + /CX에서는 사용할 수는 `Platform::IBox<T>` nullable 값 형식 매개 변수를 지 원하는 공용 메서드를 노출 하는 형식입니다. 다음 예제에서는 C + + /cli는 C# 호출자가 인수 중 하나에 대해 null을 전달 하는 경우 null을 반환 하는 CX 공용 메서드.

[!code-cpp[cx_boxing#02](../cppcx/codesnippet/CPP/cx_boxing/class1.h#02)]

C# XAML 클라이언트에서 이러한 메서드를 다음과 같이 사용할 수 있습니다.

```

// C# client code
    BoxingDemo.Class1 obj = new BoxingDemo.Class1();
    int? a = null;
    int? b = 5;
    var result = obj.Multiply(a,b); //result = null

```

## <a name="see-also"></a>참고 항목

[형식 시스템(C++/CX)](../cppcx/type-system-c-cx.md)<br/>
[캐스팅(C++/CX)](../cppcx/casting-c-cx.md)<br/>
[Visual c + + 언어 참조](../cppcx/visual-c-language-reference-c-cx.md)<br/>
[네임 스페이스 참조](../cppcx/namespaces-reference-c-cx.md)