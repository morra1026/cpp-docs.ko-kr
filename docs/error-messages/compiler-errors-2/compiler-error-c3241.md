---
title: 컴파일러 오류 C3241 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3241
dev_langs:
- C++
helpviewer_keywords:
- C3241
ms.assetid: 2ca14879-bba0-4a23-b22a-72cfff92d6a4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6f78346c91d7f103d1392081a90d982f3d99b493
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46020238"
---
# <a name="compiler-error-c3241"></a>컴파일러 오류 C3241

'method':이 메서드는 'interface' 도입 되지 않았기

함수를 명시적으로 재정의 하는 경우 함수 시그니처는 재정의 하는 함수에 대 한 선언을 정확히 일치 해야 합니다.

다음 샘플에서는 C3241 오류가 생성 됩니다.

```
// C3241.cpp
#pragma warning(disable:4199)

__interface IX12A {
   void mf();
};

__interface IX12B {
   void mf(int);
};

class CX12 : public IX12A, public IX12B { // C3241
   void IX12A::mf(int);
};
```