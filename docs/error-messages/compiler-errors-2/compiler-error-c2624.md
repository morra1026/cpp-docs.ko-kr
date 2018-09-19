---
title: 컴파일러 오류 C2624 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2624
dev_langs:
- C++
helpviewer_keywords:
- C2624
ms.assetid: 32f2ec15-a7cd-4049-a64b-131746d3152b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4db17508d9335439e861cf5489bddfab366dec1a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46109122"
---
# <a name="compiler-error-c2624"></a>컴파일러 오류 C2624

'extern' 변수를 선언 하는 로컬 클래스를 사용할 수 없습니다.

로컬 클래스 또는 구조체 선언에 사용할 수 없습니다 `extern` 변수입니다.

다음 샘플에서는 C2624를 생성합니다.

```
// C2624.cpp
int main() {
   struct C {};
   extern C ac;   // C2624
}
```