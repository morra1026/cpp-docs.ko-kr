---
title: 컴파일러 오류 C3131 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3131
dev_langs:
- C++
helpviewer_keywords:
- C3131
ms.assetid: 38f20fac-83c9-4cd9-b7b5-74ca8f650ea6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a7830e5c0ea57a7b6b6e42f020f723f1c4f80a7a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46035489"
---
# <a name="compiler-error-c3131"></a>컴파일러 오류 C3131

프로젝트에 'name' 속성과 'module' 특성이 있어야 합니다.

합니다 [모듈](../../windows/module-cpp.md) 특성 이름 매개 변수가 있어야 합니다.

다음 샘플에서는 C3131를 생성합니다.

```
// C3131.cpp
[emitidl];
[module];   // C3131
// try the following line instead
// [module (name="MyLib")];

[public]
typedef long int LongInt;
```