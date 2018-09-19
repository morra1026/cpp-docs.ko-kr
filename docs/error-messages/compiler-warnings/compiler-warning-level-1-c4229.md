---
title: 컴파일러 경고 (수준 1) C4229 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4229
dev_langs:
- C++
helpviewer_keywords:
- C4229
ms.assetid: aadfc83b-1e5f-4229-bd0a-9c10a5d13182
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e485f4e49859a12b17eac5dd378853bb3795bd7e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064050"
---
# <a name="compiler-warning-level-1-c4229"></a>컴파일러 경고(수준 1) C4229

된 구문을 사용 했습니다: 데이터의 한정자는 무시 됩니다.

와 같은 Microsoft 한정자를 사용 하 여 `__cdecl` 데이터 선언에는 오래 된 방법입니다.

## <a name="example"></a>예제

```
// C4229.cpp
// compile with: /W1 /LD
int __cdecl counter;   // C4229 cdecl ignored
```