---
title: 컴파일러 경고 (수준 4) C4565 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4565
dev_langs:
- C++
helpviewer_keywords:
- C4565
ms.assetid: a71f1341-a4a1-4060-ad1e-9322531883ed
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c25f2f1fc16c6d45a7d1eddec8d3efe62db142f2
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43211264"
---
# <a name="compiler-warning-level-4-c4565"></a>컴파일러 경고(수준 4) C4565

> '*함수*': 재정의; 기호를 __declspec를 사용 하 여 이전에 선언 되었습니다 (*한정자*)

## <a name="remarks"></a>설명

두 번째 달리 정의 또는 선언에서 첫 번째 정의 또는 선언 하지 않은 및 기호를 다시 정의 되었거나 다시 선언 된 `__declspec` 한정자 (*한정자*). 이 경고는 정보 제공용입니다. 이 경고를 해결 하려면 정의 중 하나를 삭제 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4565 오류가 생성 됩니다.

```cpp
// C4565.cpp
// compile with: /W4 /LD
__declspec(noalias) void f();
void f();   // C4565
```