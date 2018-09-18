---
title: 컴파일러 오류 C3734 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3734
dev_langs:
- C++
helpviewer_keywords:
- C3734
ms.assetid: 4e2afdcc-7da9-45a1-9c96-85f25e2986e8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d304b3853986b54f9844f9e4968f7bb7d6a8af5a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46072747"
---
# <a name="compiler-error-c3734"></a>컴파일러 오류 C3734

'class': 관리되는 클래스 또는 WinRT 클래스에는 coclass를 사용할 수 없습니다.

합니다 [coclass](../../windows/coclass.md) 특성을 사용 하 여 사용할 수 없습니다 관리 되는 또는 WinRT 클래스입니다.

다음 샘플에서는 C3734를 생성하고 해결 방법을 보여 줍니다.

```
// C3734.cpp
// compile with: /clr /c
[module(name="x")];

[coclass]
ref class CMyClass {   // C3734 remove the ref keyword to resolve
};
```
