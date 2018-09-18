---
title: 컴파일러 오류 C2110 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2110
dev_langs:
- C++
helpviewer_keywords:
- C2110
ms.assetid: 48fd76ed-90d6-4a60-9c7b-f6ce9355b4ca
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 749e96748698da9b2c08e805d68e0c2ba333d22f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074905"
---
# <a name="compiler-error-c2110"></a>컴파일러 오류 C2110

'+': 두 포인터를 더할 수 없습니다.

더하기( `+` ) 연산자를 사용하여 두 포인터 값을 더하려고 했습니다.

다음 샘플에서는 C2110을 생성합니다.

```
// C2110.cpp
int main() {
   int a = 0;
   int *pa;
   int *pb;
   a = pa + pb;   // C2110
}
```