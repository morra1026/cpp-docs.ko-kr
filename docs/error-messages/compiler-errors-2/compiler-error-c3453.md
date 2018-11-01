---
title: 컴파일러 오류 C3453
ms.date: 11/04/2016
f1_keywords:
- C3453
helpviewer_keywords:
- C3453
ms.assetid: dbefdbcf-f697-4239-b7a5-1d99b85e9e7f
ms.openlocfilehash: 2b3288d02c611bf6785ca1ea7757e2283d889050
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50472724"
---
# <a name="compiler-error-c3453"></a>컴파일러 오류 C3453

'attribute': 'assembly' 한정자가 일치하지 않아 특성이 적용되지 않았습니다.

어셈블리 또는 모듈 수준 특성만 독립 실행형 명령으로 지정할 수 있습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3453을 생성합니다.

```
// C3453.cpp
// compile with: /clr /c
[assembly:System::CLSCompliant(true)]   // C3453
// try the following line instead
// [assembly:System::CLSCompliant(true)];
ref class X {};
```