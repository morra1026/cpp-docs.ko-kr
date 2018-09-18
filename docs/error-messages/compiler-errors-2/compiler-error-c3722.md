---
title: 컴파일러 오류 C3722 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3722
dev_langs:
- C++
helpviewer_keywords:
- C3722
ms.assetid: 3cb28363-5eff-4548-bd0d-d5c615846353
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9ec84898d413bd0b62c9b0d96e47ef82615a4b06
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46058980"
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