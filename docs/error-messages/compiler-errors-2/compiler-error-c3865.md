---
title: 컴파일러 오류 C3865 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3865
dev_langs:
- C++
helpviewer_keywords:
- C3865
ms.assetid: 9bc62bb0-4fb8-4856-a5cf-c7cb4029a596
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8fd5c83d922601ca4cdffe0f3772723b31e630b6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46090843"
---
# <a name="compiler-error-c3865"></a>컴파일러 오류 C3865

'calling_convention': 네이티브 멤버 함수에만 사용할 수 있습니다

호출 규칙을 관리 되는 멤버 함수 또는 전역 함수는 함수에서 사용 되었습니다. 호출 규칙 (관리 되지 않는) 네이티브 멤버 함수에만 사용할 수 있습니다.

자세한 내용은 [호출 규칙](../../cpp/calling-conventions.md)합니다.

다음 샘플에서는 C3865 오류가 생성 됩니다.

```
// C3865.cpp
// compile with: /clr
// processor: x86
void __thiscall Func(){}   // C3865

// OK
struct MyType {
   void __thiscall Func(){}
};
```