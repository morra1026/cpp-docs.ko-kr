---
title: 컴파일러 오류 C3666
ms.date: 11/04/2016
f1_keywords:
- C3666
helpviewer_keywords:
- C3666
ms.assetid: 459e51dd-cefb-4346-99b3-644f2d8b65b2
ms.openlocfilehash: aba1d3dfcf620db0f1fbaf14d0fb01745ca82659
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50465548"
---
# <a name="compiler-error-c3666"></a>컴파일러 오류 C3666

'constructor': 재정의 지정자는 'keyword' 생성자를 사용할 수 없습니다

생성자에는 재정의 지정자를 사용한 및 허용 되지 않습니다. 자세한 내용은 [재정의 지정자](../../windows/override-specifiers-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3666를 생성합니다.

```
// C3666.cpp
// compile with: /clr /c
ref struct R {
   R() new {}   // C3666
   R(int i) {}   // OK
};
```