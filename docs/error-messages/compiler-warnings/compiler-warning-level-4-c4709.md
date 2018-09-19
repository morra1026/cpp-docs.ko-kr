---
title: 컴파일러 경고 (수준 4) C4709 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4709
dev_langs:
- C++
helpviewer_keywords:
- C4709
ms.assetid: 8abfdd45-8c70-4c27-b0fb-ca0c3f0fccf9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: df12a377c3d365eaf274e58f9d573753aa1f0a57
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078987"
---
# <a name="compiler-warning-level-4-c4709"></a>컴파일러 경고(수준 4) C4709

배열 인덱스 식 내에 쉼표 연산자

쉼표는 배열 인덱스 식의 경우 컴파일러는 마지막 쉼표 뒤의 값을 사용 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4709 오류가 생성 됩니다.

```
// C4709.cpp
// compile with: /W4
#include <stdio.h>

int main()
{
    int arr[2][2];
    arr[0][0] = 10;
    arr[0][1] = 11;

    // Prints 10, not 11
    printf_s("\n%d",arr[0][1,0]);   // C4709
}
```