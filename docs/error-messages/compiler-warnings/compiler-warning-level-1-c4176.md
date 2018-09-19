---
title: 컴파일러 경고 (수준 1) C4176 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4176
dev_langs:
- C++
helpviewer_keywords:
- C4176
ms.assetid: cfffb934-219a-4a63-9df6-ba54405bf766
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f173e132a2bd0d54c32fb0c2f7ae3b13dff1657d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085708"
---
# <a name="compiler-warning-level-1-c4176"></a>컴파일러 경고(수준 1) C4176

'subcomponent': #pragma 구성 요소 브라우저의 하위 구성 요소를 알 수 없습니다.

**구성 요소** pragma에 잘못된 하위 구성 요소가 포함되어 있습니다. 특정 이름에 대한 참조를 제외하려면 이름 앞에 **참조** 옵션을 사용해야 합니다.

## <a name="example"></a>예제

```
// C4176.cpp
// compile with: /W1 /LD
#pragma component(browser, off, i)  // C4176
#pragma component(browser, off, references, i) // ok
```