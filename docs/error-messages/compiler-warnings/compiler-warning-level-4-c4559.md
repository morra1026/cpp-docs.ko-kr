---
title: 컴파일러 경고 (수준 4) C4559 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4559
dev_langs:
- C++
helpviewer_keywords:
- C4559
ms.assetid: ed542f60-454d-45cb-85da-987ede61b1ab
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4d5743b33f62aa954c3765b729ab5c0297b20e32
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43195578"
---
# <a name="compiler-warning-level-4-c4559"></a>컴파일러 경고(수준 4) C4559

> '*함수*': 재정의; 함수 향상 __declspec (*한정자*)

## <a name="remarks"></a>설명

두 번째 정의 또는 선언 추가한 함수를 다시 정의 되었거나 다시 선언 된 **__declspec** 한정자 (*한정자*). 이 경고는 정보 제공용입니다. 이 경고를 해결 하려면 정의 중 하나를 삭제 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4559 오류가 생성 됩니다.

```cpp
// C4559.cpp
// compile with: /W4 /LD
void f();
__declspec(noalias) void f();   // C4559
```