---
title: 컴파일러 오류 C2850 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2850
dev_langs:
- C++
helpviewer_keywords:
- C2850
ms.assetid: f3efe86c-4168-4e76-a133-3f8314c69f51
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 89e3cc7065ed5a0a91ad77ea5a6c44b38622b8e3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46057888"
---
# <a name="compiler-error-c2850"></a>컴파일러 오류 C2850

'construct': 파일 범위에만 추가할 수 중첩된 된 구문에 사용할 수 없습니다.

일부 pragma 등과 같은 구문을 전역 범위에만 나타날 수 있습니다.

다음 샘플에서는 C2850 오류가 생성 됩니다.

```
// C2850.cpp
// compile with: /c /Yc
// try the following line instead
// #pragma hdrstop
namespace X {
   #pragma hdrstop   // C2850
};
```