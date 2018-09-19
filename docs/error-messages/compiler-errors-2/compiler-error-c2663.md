---
title: 컴파일러 오류 C2663 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2663
dev_langs:
- C++
helpviewer_keywords:
- C2663
ms.assetid: 1e93e368-fd52-42bf-9908-9b6df467c8c9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fed35dcce056eb3d2a660c154e94b8058563dba7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46083693"
---
# <a name="compiler-error-c2663"></a>컴파일러 오류 C2663

'function': 오버 로드에 숫자 'this'이 포인터에 대 한 법적 변환이 있어야

컴파일러가 변환 하지 못했습니다 `this` 를 멤버 함수의 오버 로드 된 버전입니다.

비-를 호출 하 여이 오류를 발생할 수 있습니다`const` 에 대해 멤버 함수는 `const` 개체입니다.  가능한 해결 방법:

1. 제거 된 `const` 개체 선언에서.

1. 추가 `const` 멤버 함수 오버 로드 중 하나에 있습니다.

다음 샘플에서는 C2663를 생성합니다.

```
// C2663.cpp
struct C {
   void f() volatile {}
   void f() {}
};

struct D {
   void f() volatile;
   void f() const {}
};

const C *pcc;
const D *pcd;

int main() {
   pcc->f();    // C2663
   pcd->f();    // OK
}
```