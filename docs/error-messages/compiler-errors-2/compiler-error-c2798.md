---
title: 컴파일러 오류 C2798 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2798
dev_langs:
- C++
helpviewer_keywords:
- C2798
ms.assetid: fb0cd861-b228-4f81-8090-e28344a727e0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 88241989d54e1a068b226b59091a381f531dee9e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46028859"
---
# <a name="compiler-error-c2798"></a>컴파일러 오류 C2798

'super::member' 모호합니다.

사용 하 여 참조 하는 멤버를 포함 하는 다중 상속된 구조 [super](../../cpp/super.md)합니다. 오류를 해결할 수 있습니다.

- B1 또는 B2 D.의 상속 목록에서 제거합니다.

- -B2에서 B1의 데이터 멤버의 이름을 변경 합니다.

다음 샘플에서는 C2798 오류가 생성 됩니다.

```
// C2798.cpp
struct B1 {
   int i;
};

struct B2 {
   int i;
};

struct D : B1, B2 {
   void g() {
      __super::i = 4; // C2798
   }
};
```