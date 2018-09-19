---
title: 컴파일러 경고 (수준 1) C4103 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4103
dev_langs:
- C++
helpviewer_keywords:
- C4103
ms.assetid: 9021b514-375e-4d62-b261-ccb06f299e8e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1942acc2d9c5c274806e06127f9f98d4bfcb5077
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085539"
---
# <a name="compiler-warning-level-1-c4103"></a>컴파일러 경고 (수준 1) C4103

'filename': 맞춤 헤더를 포함 한 후에 변경할 #pragma pack(pop) 없기 때문일 수 있습니다

압축 클래스의 레이아웃에 영향을 줍니다 및 일반적으로 헤더 파일에서 변경 내용을 압축을 하는 경우 문제가 가능성이 있습니다.

사용할 #pragma [팩](../../preprocessor/pack.md)(pop)이이 경고를 해결 하려면 헤더 파일을 종료 하기 전에 합니다.

다음 샘플에서는 C4103 오류가 생성 됩니다.

```
// C4103.h
#pragma pack(push, 4)

// defintions and declarations

// uncomment the following line to resolve
// #pragma pack(pop)
```

그리고

```
// C4103.cpp
// compile with: /LD /W1
#include "c4103.h"   // C4103
```