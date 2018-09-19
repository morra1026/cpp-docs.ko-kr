---
title: 컴파일러 오류 C3611 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3611
dev_langs:
- C++
helpviewer_keywords:
- C3611
ms.assetid: 42f3e320-41de-420a-bd05-8924cab765aa
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6bc7f1f96e774c7b0dd9df2f760d9c45a522de1c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039649"
---
# <a name="compiler-error-c3611"></a>컴파일러 오류 C3611

'function': 봉인 된 함수는 순수 지정자를 사용할 수 없습니다

봉인 된 함수를 잘못 선언 되었습니다.  자세한 내용은 [봉인](../../windows/sealed-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3611를 생성합니다.

```
// C3611.cpp
// compile with: /clr /c

ref struct V {
   virtual void Test() sealed = 0;   // C3611
   virtual void Test2() sealed;   // OK
   virtual void Test3() = 0;   // OK
};
```