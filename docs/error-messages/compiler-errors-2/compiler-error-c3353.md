---
title: 컴파일러 오류 C3353 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3353
dev_langs:
- C++
helpviewer_keywords:
- C3353
ms.assetid: 5699c04b-d504-46ce-bf71-c200318fed71
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 63316a5a74c3981ec0f68d949eba654f8d6bbfef
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110200"
---
# <a name="compiler-error-c3353"></a>컴파일러 오류 C3353

'delegate': 대리자는 전역 함수 또는 관리되는 또는 WinRT 형식의 멤버 함수에서만 만들어질 수 있습니다.

대리자를 사용 하 여 선언 된 [대리자](../../windows/delegate-cpp-component-extensions.md) 키워드를 전역 범위에서 선언할 수 있습니다.

다음 샘플에서는 C3353을 생성합니다.

```
// C3353.cpp
// compile with: /clr
delegate int f;   // C3353
```