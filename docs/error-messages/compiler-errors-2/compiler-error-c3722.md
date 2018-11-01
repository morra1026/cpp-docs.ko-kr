---
title: 컴파일러 오류 C3722
ms.date: 11/04/2016
f1_keywords:
- C3722
helpviewer_keywords:
- C3722
ms.assetid: 3cb28363-5eff-4548-bd0d-d5c615846353
ms.openlocfilehash: d3c721490e0af32d91fcc51412e3c02b6a2d7f67
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50451001"
---
# <a name="compiler-error-c3722"></a>컴파일러 오류 C3722

일반 이벤트 허용 되지 않습니다.

컴파일러는 제네릭 클래스, 구조체 및 함수에만 허용 합니다.  자세한 내용은 [제네릭](../../windows/generics-cpp-component-extensions.md)을 참조하세요.

다음 샘플에서는 C3722를 생성합니다.

```
// C3722.cpp
// compile with: /clr
generic <typename T>
public delegate void MyEventHandler(System::Object^ sender, System::EventArgs^ e, T optional);

generic <class T>
public ref struct MyButton {
   generic<typename U>
   event MyEventHandler<U>^ Click;   // C3722
};
```