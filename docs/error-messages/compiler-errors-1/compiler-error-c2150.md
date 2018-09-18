---
title: 컴파일러 오류 C2150 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2150
dev_langs:
- C++
helpviewer_keywords:
- C2150
ms.assetid: 21e82a10-c1d4-4c0d-9dc6-c5d92ea42a31
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ef0920c98fe59fe5bca49bba4c62a486a61c0a55
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46024713"
---
# <a name="compiler-error-c2150"></a>컴파일러 오류 C2150

> '*식별자*': 비트 필드 형식은 'int', 'signed int' 또는 'unsigned int' 있어야 합니다.

비트 필드의 기본 형식 되어야 할 `int`, `signed int`, 또는 `unsigned int`합니다.

## <a name="example"></a>예제

이 샘플에서는 C2150을 발생할 수 있는 방법 및 해결 하는 방법을 보여 줍니다.

```cpp
// C2150.cpp
// compile with: /c
struct A {
   float a : 8;    // C2150
   int i : 8;      // OK
};
```