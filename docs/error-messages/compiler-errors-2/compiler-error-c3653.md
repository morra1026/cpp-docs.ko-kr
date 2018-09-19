---
title: 컴파일러 오류 C3653 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3653
dev_langs:
- C++
helpviewer_keywords:
- C3653
ms.assetid: 316549d7-f7ef-4578-a2ba-57adc8aac527
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8d0409317cb0cdf6a248554cba2e18d7f9d2e0e0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46019005"
---
# <a name="compiler-error-c3653"></a>컴파일러 오류 C3653

'function': 명명된 된 재정의로 사용할 수 없습니다: 찾은; 재정의 되는 함수 함수를 사용 하 여 명시적으로 이름을 하 였는:: operator?

명시적 재정의 모든 인터페이스에서 찾을 수 없는 함수를 지정 합니다. 자세한 내용은 [명시적으로 재정의](../../windows/explicit-overrides-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3653를 생성합니다.

```
// C3653.cpp
// compile with: /clr
public interface struct I {
   void h();
};

public ref struct X : public I {
   virtual void f() new sealed = J {};   // C3653 no J in scope
   virtual void g() {}   // OK
   virtual void h() new sealed = I::h {};   // OK
};
```