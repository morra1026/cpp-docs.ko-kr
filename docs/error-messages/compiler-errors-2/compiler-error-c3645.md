---
title: 컴파일러 오류 C3645
ms.date: 11/04/2016
f1_keywords:
- C3645
helpviewer_keywords:
- C3645
ms.assetid: 346da528-ae86-4cd0-9654-f41bee26ac0d
ms.openlocfilehash: f733de6920e00f1f53c87884a7a334e575bceb06
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50500336"
---
# <a name="compiler-error-c3645"></a>컴파일러 오류 C3645

'function': __clrcall을 네이티브 코드로 컴파일된 함수에 사용할 수 없습니다

함수에서 일부 키워드의 현재 상태를 사용 하면 함수가를 네이티브로 컴파일하도록 합니다.

## <a name="example"></a>예제

다음 샘플 C3645를 생성합니다.

```
// C3645.cpp
// compile with: /clr /c
#pragma unmanaged
int __clrcall dog() {}   // C3645
```