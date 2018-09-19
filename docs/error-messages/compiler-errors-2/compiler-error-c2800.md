---
title: 컴파일러 오류 C2800 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2800
dev_langs:
- C++
helpviewer_keywords:
- C2800
ms.assetid: a2f1a590-9fe6-44cb-ad09-b4505ef47c6a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 23441361ea0c8dbc241f5bf655186f0399b6b42f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016379"
---
# <a name="compiler-error-c2800"></a>컴파일러 오류 C2800

'operator o'를 오버 로드할 수 없습니다.

다음 연산자를 오버 로드할 수 없습니다: 클래스 멤버 액세스 (`.`), 멤버 포인터 (`.*`), 범위 결정 (`::`), 조건식 (`? :`), 및 `sizeof`합니다.

다음 샘플에서는 C2800 오류가 생성 됩니다.

```
// C2800.cpp
// compile with: /c
class C {
   operator:: ();   // C2800
};
```