---
title: 컴파일러 경고 (수준 1) C4806 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4806
dev_langs:
- C++
helpviewer_keywords:
- C4806
ms.assetid: 79eb74cd-b925-4b5b-84e1-8ae6f33e38b3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b580500c3887fe60b7864280ad5ca1804752f2ae
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062607"
---
# <a name="compiler-warning-level-1-c4806"></a>컴파일러 경고(수준 1) C4806

'operation': 안전하지 않은 연산입니다. 'type' 형식의 값('type' 형식으로 확장)이 주어진 상수와 같을 수 없습니다.

이 메시지는 `b == 3`과 같은 코드에 대해 경고합니다. 여기서 `b` 는 `bool`형식입니다. 승격 규칙으로 인해 `bool` 이 `int`로 승격됩니다. 유효하지만 **true**가 될 수 없습니다. 다음 샘플에서는 C4806을 생성합니다.

```
// C4806.cpp
// compile with: /W1
int main()
{
   bool b = true;
   // try..
   // int b = true;

   if (b == 3)   // C4806
   {
      b = false;
   }
}
```