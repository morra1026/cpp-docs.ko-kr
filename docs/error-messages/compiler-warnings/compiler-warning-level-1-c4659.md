---
title: 컴파일러 경고 (수준 1) C4659 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4659
dev_langs:
- C++
helpviewer_keywords:
- C4659
ms.assetid: e29ba8db-7917-43f6-8e34-868b752279ae
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d00c54fa77d68722b2e47a9d49832911b398deca
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110063"
---
# <a name="compiler-warning-level-1-c4659"></a>컴파일러 경고(수준 1) C4659

\#pragma 'pragma': 사용 하 여 예약 된 세그먼트 '세그먼트' 동작이 정의 되지 않았습니다, #pragma 주석 (linker,...)를 사용 합니다.

.Drectve 옵션을 링커에 옵션 전달 하는 데 사용 되었습니다. Pragma를 사용 하는 대신 [주석](../../preprocessor/comment-c-cpp.md) 링커 옵션을 전달 합니다.

```
// C4659.cpp
// compile with: /W1 /LD
#pragma code_seg(".drectve")   // C4659
```