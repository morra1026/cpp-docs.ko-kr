---
title: 컴파일러 경고 (수준 1) C4556 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- xml
- C4556
dev_langs:
- C++
helpviewer_keywords:
- C4556
ms.assetid: e4c0e296-b747-4db1-9608-30b8b74feac2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 987e4dc3ba6aea7dcb01dc05cd94c45baced05b8
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43211030"
---
# <a name="compiler-warning-level-1-c4556"></a>컴파일러 경고(수준 1) C4556

> 직접 실행 내장 인수 값 '*값*'범위를 벗어났습니다'*lowerbound* - *자체도*'

## <a name="remarks"></a>설명

내장 함수는 하드웨어 명령을 일치합니다. 하드웨어 명령에는 고정된 비트 상수를 인코딩할 수 있습니다. 하는 경우 *값* 는 범위를 벗어났거나 인코딩할 수 없으므로 적절 합니다. 컴파일러는 추가 된 비트를 자릅니다.

## <a name="example"></a>예제

다음 샘플에서는 C4556 오류가 생성 됩니다.

```cpp
// C4556.cpp
// compile with: /W1
// processor: x86 IPF
#include <xmmintrin.h>

void test()
{
   __m64 m;
   _m_pextrw(m, 5);   // C4556
}

int main()
{
}
```