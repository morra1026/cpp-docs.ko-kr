---
title: 컴파일러 경고 (수준 1) C4076 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4076
dev_langs:
- C++
helpviewer_keywords:
- C4076
ms.assetid: 04581066-313a-4a11-bb60-721e6d038d75
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 928b0a78c09773e334c1a291877b74304dab66ec
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43198480"
---
# <a name="compiler-warning-level-1-c4076"></a>컴파일러 경고(수준 1) C4076

> '*형식 한정자*': 형식을 사용 하 여 사용할 수 없습니다 '*typename*'

## <a name="remarks"></a>설명

형식 한정자를 인지 **서명** 하거나 **부호 없는**, 정수가 아닌 형식과 사용할 수 없습니다. *형식 한정자* 무시 됩니다.
  
## <a name="example"></a>예제  

다음 샘플에서는 C4076; 이 문제를 해결 하려면 제거 합니다 **부호 없는** 형식 한정자:

```cpp
// C4076.cpp  
// compile with: /W1 /LD  
unsigned double x;   // C4076  
```