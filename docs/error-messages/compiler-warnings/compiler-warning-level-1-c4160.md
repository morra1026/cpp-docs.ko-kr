---
title: 컴파일러 경고 (수준 1) C4160 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4160
dev_langs:
- C++
helpviewer_keywords:
- C4160
ms.assetid: a9610cb7-cac4-4a74-8b4e-049030ebb92b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c62bf021065870f2ddd64cd7ee08cc00504cf7bd
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43219677"
---
# <a name="compiler-warning-level-1-c4160"></a>컴파일러 경고(수준 1) C4160

> #<a name="pragma-pop--did-not-find-previously-pushed-identifier-identifier"></a>pragma (pop,...): 이전에 푸시한 식별자를 찾을 수 없습니다 '*식별자*'

## <a name="remarks"></a>설명

소스 코드의 pragma 문에서 푸시되지 않은 식별자를 표시하려고 합니다. 이 경고를 방지하려면 표시 중인 식별자가 올바르게 푸시되었는지 확인합니다.

## <a name="example"></a>예제

다음 예제에서는 C4160을 생성 하 고를 해결 하는 방법을 보여 줍니다.

```cpp
// C4160.cpp
// compile with: /W1
#pragma pack(push)

#pragma pack(pop, id)   // C4160
// use identifier when pushing to resolve the warning
// #pragma pack(push, id)

int main() {
}
```