---
title: 컴파일러 오류 C2341 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2341
dev_langs:
- C++
helpviewer_keywords:
- C2341
ms.assetid: aa2a7da5-e1c8-4225-9939-5bdc50158f31
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: adac1e6f6e5f5d58b6091a389537a42f0e496b31
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46020201"
---
# <a name="compiler-error-c2341"></a>컴파일러 오류 C2341

'section n': 세그먼트를 사용 하 여 #pragma data_seg, code_seg 또는 section을 사용 하 여 정의 해야 합니다

[할당할](../../cpp/allocate.md) 문이 아직 정의한 세그먼트 참조 [code_seg](../../preprocessor/code-seg.md), [data_seg](../../preprocessor/data-seg.md), 또는 [섹션](../../preprocessor/section.md) pragma입니다.

다음 샘플에서는 C2341를 생성합니다.

```
// C2341.cpp
// compile with: /c
__declspec(allocate(".test"))   // C2341
int j = 1;
```

해결 방법:

```
// C2341b.cpp
// compile with: /c
#pragma data_seg(".test")
__declspec(allocate(".test"))
int j = 1;
```