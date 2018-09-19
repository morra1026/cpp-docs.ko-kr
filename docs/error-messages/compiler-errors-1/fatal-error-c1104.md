---
title: 심각한 오류 C1104 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1104
dev_langs:
- C++
helpviewer_keywords:
- C1104
ms.assetid: 45bd85c4-77d3-4d3c-b167-49c563aefb4d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e624238a1b7616ab84a655839a05cfd6899d38ea
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46048112"
---
# <a name="fatal-error-c1104"></a>심각한 오류 C1104

libid를 가져오는 동안 심각한 오류가 발생했습니다. 'message'

컴파일러가 형식 라이브러리를 가져오는 동안 문제를 발견했습니다.  예를 들어 libid를 사용하여 형식 라이브러리를 지정하고 `no_registry`도 지정할 수는 없습니다.

자세한 내용은 [#import 지시문](../../preprocessor/hash-import-directive-cpp.md)합니다.

다음 샘플에서는 C1104를 생성합니다.

```
// C1104.cpp
#import "libid:11111111.1111.1111.1111.111111111111" version("4.0") lcid("9") no_registry auto_search   // C1104
```