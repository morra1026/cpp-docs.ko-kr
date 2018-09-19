---
title: 컴파일러 오류 C2806 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2806
dev_langs:
- C++
helpviewer_keywords:
- C2806
ms.assetid: 7c9ff1f4-1590-4c47-991d-b1075a173b48
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 01cf48170c8fc8b73f9c4cbe36c051a8daff4314
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46043640"
---
# <a name="compiler-error-c2806"></a>컴파일러 오류 C2806

'operator o'에 정식 매개 변수가 너무 많습니다.

오버 로드 된 연산자는 매개 변수가 너무 많습니다.

다음 샘플에서는 C2806 오류가 생성 됩니다.

```
// C2806.cpp
// compile with: /c
class X {
public:
   X operator++ ( int, int );   // C2806 more than 1 parameter
   X operator++ ( int );   // OK
} ;
```