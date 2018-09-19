---
title: 컴파일러 오류 C3320 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3320
dev_langs:
- C++
helpviewer_keywords:
- C3320
ms.assetid: 2ef72d9a-1f1d-4b2e-b244-9fd3f3e70cb6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b67d419630d59902270638213ce7a79dd8b9e0c4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078441"
---
# <a name="compiler-error-c3320"></a>컴파일러 오류 C3320

'type': 형식은 모듈의 'name' 속성과 같은 이름을 사용할 수 없습니다.

에 전달 된 매개 변수는 내보낸된 사용자 정의 형식 (UDT), 구조체, 클래스, 열거형 또는 공용 구조체 수 있는 동일한 이름을 사용할 수 없습니다는 [모듈](../../windows/module-cpp.md) 특성의 name 속성입니다.

## <a name="example"></a>예제

다음 샘플에서는 C3320을 생성합니다.

```cpp
// C3320.cpp
#include "unknwn.h"
[module(name="xx")];

[export] struct xx {   // C3320
// Try the following line instead
// [export] struct yy {
   int i;
};
```