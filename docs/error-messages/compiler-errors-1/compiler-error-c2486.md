---
title: 컴파일러 오류 C2486 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2486
dev_langs:
- C++
helpviewer_keywords:
- C2486
ms.assetid: 436da349-6461-4e32-bfca-4f3e620108e2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 106d70c031a6981157875c86b1332bbe3be8a668
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46081730"
---
# <a name="compiler-error-c2486"></a>컴파일러 오류 C2486

' __LOCAL_SIZE' 'naked' 특성이 있는 함수에만 사용할 수

인라인 어셈블리 함수에서 이름 `__LOCAL_SIZE` 으로 선언 된 함수에 대해 예약 된 [naked](../../cpp/naked-cpp.md) 특성입니다.

다음 샘플에서는 C2486를 생성합니다.

```
// C2486.cpp
// processor: x86
void __declspec(naked) f1() {
   __asm {
      mov   eax,   __LOCAL_SIZE
   }
}
void f2() {
   __asm {
      mov   eax,   __LOCAL_SIZE   // C2486
   }
}
```