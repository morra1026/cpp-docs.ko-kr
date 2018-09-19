---
title: 컴파일러 오류 C2563 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2563
dev_langs:
- C++
helpviewer_keywords:
- C2563
ms.assetid: 54abba68-6458-4ca5-894d-3babdb7b3552
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: eec8526df1c5ff69899dd0a2d103cb5f28d4c00c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067406"
---
# <a name="compiler-error-c2563"></a>컴파일러 오류 C2563

정식 매개 변수 목록과에서 일치 하지 않습니다.

함수 (또는 함수에 대 한 포인터) 형식 매개 변수 목록에 다른 함수 (또는 멤버 함수에 대 한 포인터)의 일치 하지 않습니다. 결과적으로, 함수 또는 포인터에 할당 될 수 없습니다.

다음 샘플에서는 C2563 오류가 생성 됩니다.

```
// C2563.cpp
void func( int );
void func( int, int );
int main() {
   void *fp();
   fp = func;   // C2563
}
```