---
title: 컴파일러 오류 C3271
ms.date: 11/04/2016
f1_keywords:
- C3271
helpviewer_keywords:
- C3271
ms.assetid: 16d8bd1d-2e30-4c6a-a07f-0c4f3342fab5
ms.openlocfilehash: f94ef54408584e40dc406935e36053352ecf38e8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50651865"
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
