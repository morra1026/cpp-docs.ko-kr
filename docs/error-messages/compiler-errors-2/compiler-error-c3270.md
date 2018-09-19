---
title: 컴파일러 오류 C3270 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3270
dev_langs:
- C++
helpviewer_keywords:
- C3270
ms.assetid: 70e6e76b-7415-48f5-a61e-2ed50caf08e4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9c421ee1efa56e7f7e9a9444bafa15d392a78ae3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053494"
---
# <a name="compiler-error-c3270"></a>컴파일러 오류 C3270

'field': FieldOffset 특성은 필요한 StructLayout(Explicit) 컨텍스트에서만 사용할 수 있습니다.

필드 표시 되어 있으므로 **FieldOffset**때만 허용 되는 **structlayout (explicit)** 적용 됩니다.

다음 샘플에서는 C3270을 생성합니다.

```
// C3270_2.cpp
// compile with: /clr /c
using namespace System::Runtime::InteropServices;

[ StructLayout(LayoutKind::Sequential) ]
// try the following line instead
// [ StructLayout(LayoutKind::Explicit) ]
public value struct MYUNION
{
   [FieldOffset(0)] int a;   // C3270
   // ...
};
```
