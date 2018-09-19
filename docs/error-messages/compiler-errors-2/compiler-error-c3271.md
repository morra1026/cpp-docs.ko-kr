---
title: 컴파일러 오류 C3271 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3271
dev_langs:
- C++
helpviewer_keywords:
- C3271
ms.assetid: 16d8bd1d-2e30-4c6a-a07f-0c4f3342fab5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d30a203f37e09b84a62863c26b2e0c59c270369a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46091857"
---
# <a name="compiler-error-c3271"></a>컴파일러 오류 C3271

'member': FieldOffset 특성에 대한 값 'value'가 잘못되었습니다.

**FieldOffset** 특성에 음수가 전달되었습니다.

다음 샘플에서는 C3271을 생성합니다.

```
// C3271.cpp
// compile with: /clr /c
using namespace System;
using namespace System::Runtime::InteropServices;

[StructLayout(LayoutKind::Explicit)]
value class MyStruct1 {
   public: [FieldOffset(0)] int a;
   public: [FieldOffset(-1)] long b;   // C3271
};
```
