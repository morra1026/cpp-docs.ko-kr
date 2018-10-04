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
ms.openlocfilehash: a10c91f34cd00b8524a047131e9a39b901c83fce
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48788593"
---
# <a name="compiler-error-c3455"></a>컴파일러 오류 C3455

'attribute': 해당 인수와 일치하는 특성 생성자가 없습니다.

잘못된 값이 특성을 선언하는 데 사용되었습니다.  참조 [특성](../../windows/attributes/attribute.md) 자세한 내용은 합니다.

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