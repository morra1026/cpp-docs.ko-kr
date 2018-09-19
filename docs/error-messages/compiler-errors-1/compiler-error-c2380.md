---
title: 컴파일러 오류 C2380 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2380
dev_langs:
- C++
helpviewer_keywords:
- C2380
ms.assetid: 717b1e6e-ddfe-4bac-a5f3-7f9a4dcb1572
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8e4dae59f686a1d2fe9f80a4f3f4c47ea6b7ea2d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46065480"
---
# <a name="compiler-error-c2380"></a>컴파일러 오류 C2380

형식 앞에 'identifier' (반환 형식 또는 클래스 이름에 현재 잘못 된 재정의 사용 하 여 생성자?)

생성자 값을 반환 하거나 클래스 이름을 재정의 합니다.

다음 샘플에서는 C2326을 생성합니다.

```
// C2380.cpp
// compile with: /c
class C {
public:
   int C();   // C2380, specifies an int return
   int C;   // C2380, redefinition of i
   C();   // OK
};
```