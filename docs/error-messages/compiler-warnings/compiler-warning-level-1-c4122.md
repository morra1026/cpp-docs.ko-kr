---
title: 컴파일러 경고 (수준 1) C4122 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4122
dev_langs:
- C++
helpviewer_keywords:
- C4122
ms.assetid: 9a83eb0d-8708-42f7-988a-b0b6f2f646a0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 37f7928b1aa89eb66da95b4383084b2011387e0e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075421"
---
# <a name="compiler-warning-level-1-c4122"></a>컴파일러 경고(수준 1) C4122

'function': alloc_text는 C 링크가 있는 함수에만 적용될 수 있습니다.

**alloc_text** pragma는 **extern c**로 선언된 함수에만 적용됩니다. 외부 C++ 함수와 함께 사용할 수 없습니다.

pragma가 무시됩니다.