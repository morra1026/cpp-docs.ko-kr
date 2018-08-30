---
title: 컴파일러 경고 (수준 1) C4612 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4612
dev_langs:
- C++
helpviewer_keywords:
- C4612
ms.assetid: 21ac02b2-51cd-4aff-9b70-d543511d5962
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 10a0a5640386f5e5673f39d6c2c76ee18fcc7ba7
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43210732"
---
# <a name="compiler-warning-level-1-c4612"></a>컴파일러 경고(수준 1) C4612

> 포함 파일 이름에 오류가 있습니다.

## <a name="remarks"></a>설명

파일 이름이 잘못되었거나 누락된 경우 **#pragma include_alias** 에서 이 경고가 발생합니다.

에 대 한 인수는 **#pragma include_alias** 문은 견적 폼을 사용할 수 있습니다 ("*filename*") 또는 꺾쇠 괄호 양식 (\<*filename*>), 둘 다 해야 하지만 동일한 형식을 사용 합니다.

## <a name="example"></a>예제

```cpp
// C4612.cpp
// compile with: /W1 /LD
#pragma include_alias("StandardIO", <stdio.h>) // C4612
```