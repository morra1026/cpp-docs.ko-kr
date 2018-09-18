---
title: 컴파일러 오류 C3797 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3797
dev_langs:
- C++
helpviewer_keywords:
- C3797
ms.assetid: ab27ff34-8c1d-4297-b004-9e39bd3a4f25
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3ac1ded1c95f7e8bea9598e468010c75d8bd917a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46033422"
---
# <a name="compiler-error-c3797"></a>컴파일러 오류 C3797

'override': 이벤트 선언 (에 배치 해야 이벤트 추가/remove/raise 메서드에 대신) 하는 재정의 지정자를 사용할 수 없습니다

다른 trivial 이벤트를 사용 하 여 trivial 이벤트 (명시적으로 정의 된 접근자 메서드 없이 이벤트)를 재정의할 수 없습니다. 재정의 하는 이벤트 접근자 함수를 사용 하 여 해당 동작을 정의 해야 합니다.

자세한 내용은 [이벤트](../../windows/event-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3797를 생성합니다.

```
// C3797.cpp
// compile with: /clr /c
delegate void MyDel();

ref class Class1 {
public:
   virtual event MyDel ^ E;
};

ref class Class2 : public Class1 {
public:
   virtual event MyDel ^ E override;   // C3797
};

// OK
ref class Class3 : public Class1 {
public:
   virtual event MyDel ^ E {
      void add(MyDel ^ d) override {}
      void remove(MyDel ^ d) override {}
   }
};
```