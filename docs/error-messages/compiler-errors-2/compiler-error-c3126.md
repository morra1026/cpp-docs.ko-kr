---
title: 컴파일러 오류 C3126 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3126
dev_langs:
- C++
helpviewer_keywords:
- C3126
ms.assetid: e72658a3-5d85-4a31-89a4-dbc3d475973d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f794565c9d8054d4b66e7817b5d63fb13795ac3e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46021676"
---
# <a name="compiler-error-c3126"></a>컴파일러 오류 C3126

관리 되는 ' type' 내부 ' union' 공용 구조체를 정의할 수 없습니다.

관리 되는 형식 내에서 공용 구조체를 정의할 수 없습니다.

다음 샘플에서는 C3126 오류가 생성 됩니다.

```
// C3126_2.cpp
// compile with: /clr /c
ref class Test
{
   union x
   {   // C3126
      int a;
      int b;
   };
};
```
