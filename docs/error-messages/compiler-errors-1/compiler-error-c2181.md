---
title: 컴파일러 오류 C2181
ms.date: 11/04/2016
f1_keywords:
- C2181
helpviewer_keywords:
- C2181
ms.assetid: d52b2fe4-566a-40a9-b8e2-8dce1f287668
ms.openlocfilehash: a676794b5dedd17cfb973de36d3771ef1130a786
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50527311"
---
# <a name="compiler-error-c2181"></a>컴파일러 오류 C2181

if와 짝을 이루지 않는 잘못된 else문입니다.

각 `else` 에는 해당하는 `if`가 있어야 합니다.

다음 샘플에서는 C2181을 생성합니다.

```
// C2181.cpp
int main() {
   int i = 0;
   else   // C2181
      i = 1;
}
```

해결 방법:

```
// C2181b.cpp
int main() {
   int i = 0;
   if(i)
      i = 0;
   else
      i = 1;
}
```