---
title: 컴파일러 오류 C2378 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2378
dev_langs:
- C++
helpviewer_keywords:
- C2378
ms.assetid: 507a91c6-ca72-48df-b3a4-2cf931c86806
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5aa4b8ecef6be2149132c9ccf533285cd0bb7f7d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46021826"
---
# <a name="compiler-error-c2378"></a>컴파일러 오류 C2378

'identifier': 재정의. 형식 정의를 사용하여 기호를 오버로드할 수 없습니다.

식별자가 `typedef`로 다시 정의되었습니다.

다음 샘플에서는 C2378을 생성합니다.

```
// C2378.cpp
// compile with: /c
int i;
typedef int i;   // C2378
typedef int b;   // OK
```