---
title: 컴파일러 오류 C2092 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2092
dev_langs:
- C++
helpviewer_keywords:
- C2092
ms.assetid: 037e44ae-16c8-489a-a512-dcdf7f7795a6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3a0b8f65f58ffe65abee0f15eb511f7857657597
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46072487"
---
# <a name="compiler-error-c2092"></a>컴파일러 오류 C2092

'배열 name' 배열 요소 형식은 함수 일 수 없습니다.

함수의 배열은 허용 되지 않습니다. 함수에 대 한 포인터의 배열을 사용 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2092 오류가 생성 됩니다.

```
// C2092.cpp
typedef void (F) ();
typedef F AT[10];   // C2092
```

## <a name="example"></a>예제

해결 방법:

```
// C2092b.cpp
// compile with: /c
typedef void (F) ();
typedef F * AT[10];
```