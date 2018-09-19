---
title: 컴파일러 경고 (수준 1) C4616 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4616
dev_langs:
- C++
helpviewer_keywords:
- C4616
ms.assetid: 71e15265-c5bc-42ce-a6a9-4879892472b1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 59b81211b61db6b2537a007a20697c61a02a290a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094447"
---
# <a name="compiler-warning-level-1-c4616"></a>컴파일러 경고(수준 1) C4616

\#pragma 경고: 경고 번호 '번호' 올바른 컴파일러 경고가 아니라

에 지정 된 경고 번호를 [경고](../../preprocessor/warning.md) pragma를 다시 할당할 수 없습니다. Pragma가 무시 되었습니다.

다음 샘플에서는 C4616 오류가 생성 됩니다.

```
// C4616.cpp
// compile with: /W1 /c
#pragma warning( disable : 0 )   // C4616
#pragma warning( disable : 999 )   // OK
#pragma warning( disable : 4998 )   // OK
```