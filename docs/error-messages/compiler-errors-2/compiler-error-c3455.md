---
title: 컴파일러 오류 C3455 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3455
dev_langs:
- C++
helpviewer_keywords:
- C3455
ms.assetid: 218e5cfe-5391-4eeb-81c2-85c47e3a6cd2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5d26a8f3e404eaa19a102be4cb3f11350c4fe674
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46089361"
---
# <a name="compiler-error-c3455"></a>컴파일러 오류 C3455

'attribute': 해당 인수와 일치하는 특성 생성자가 없습니다.

잘못된 값이 특성을 선언하는 데 사용되었습니다.  자세한 내용은 [attribute](../../windows/attribute.md) 를 참조하세요.

## <a name="example"></a>예제

다음 샘플에서는 C3455를 생성합니다.

```
// C3455.cpp
// compile with: /clr /c
using namespace System;

[attribute("MyAt")]   // C3455
// try the following line instead
// [attribute(All)]
ref struct MyAttr {
   MyAttr() {}
};
```