---
title: 컴파일러 오류 C2357 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2357
dev_langs:
- C++
helpviewer_keywords:
- C2357
ms.assetid: d1083945-0ea2-4385-9e66-8c665978806c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2d6468774947ed92630d0e10badc341c5841a5aa
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46025440"
---
# <a name="compiler-error-c2357"></a>컴파일러 오류 C2357

'identifier': 'type' 형식 함수 여야

코드의 버전을 선언 합니다 `atexit` 버전이 일치 하지 않는 함수는 컴파일러에서 내부적으로 선언 합니다. 선언 `atexit` 다음과 같습니다.

```
int __cdecl atexit(void (__cdecl *)());
```

자세한 내용은 [init_seg](../../preprocessor/init-seg.md)합니다.

다음 샘플에서는 C2357 오류가 생성 됩니다.

```
// C2357.cpp
// compile with: /c
// C2357 expected
#pragma warning(disable : 4075)
// Uncomment the following line to resolve.
// int __cdecl myexit(void (__cdecl *)());
#pragma init_seg(".mine$m",myexit)
```