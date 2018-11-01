---
title: 컴파일러 오류 C3197
ms.date: 11/04/2016
f1_keywords:
- C3197
helpviewer_keywords:
- C3197
ms.assetid: 4e385c3b-222e-425c-9612-46e83ed41650
ms.openlocfilehash: be9b7dadb4f67a6392cd7a2c46caf61d983e79eb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50466019"
---
# <a name="compiler-error-c3197"></a>컴파일러 오류 C3197

'keyword': 정의에 사용할 수 있습니다

키워드는 선언에서 사용 했지만 정의에 유효 합니다.

다음 샘플에서는 C3197를 생성합니다.

```
// C3197.cpp
// compile with: /clr /c
ref struct R abstract;   // C3197
ref struct R abstract {};   // OK

public ref class MyObject;   // C3197
ref class MyObject;   // OK
public ref class MyObject {};   // OK
```