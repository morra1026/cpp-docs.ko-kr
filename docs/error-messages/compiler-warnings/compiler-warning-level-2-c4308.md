---
title: 컴파일러 경고 (수준 2) C4308 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4308
dev_langs:
- C++
helpviewer_keywords:
- C4308
ms.assetid: d4e5c53c-71b2-4bbc-8a7c-3a2a3180d9d9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ddb57d4d603be3182be8a77dc020ce0e0a673115
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039636"
---
# <a name="compiler-warning-level-2-c4308"></a>컴파일러 경고(수준 2) C4308

음의 정수 상수가 부호 없는 형식으로 변환

음의 정수 상수는 부호 없는 형식으로 변환 하는 식. 식의 결과 아마도 의미가 없습니다.

## <a name="example"></a>예제

```
// C4308.cpp
// compile with: /W2
unsigned int u = (-5 + 3U);   // C4308

int main()
{
}
```