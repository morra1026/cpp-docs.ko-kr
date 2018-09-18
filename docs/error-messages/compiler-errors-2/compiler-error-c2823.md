---
title: 컴파일러 오류 C2823 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2823
dev_langs:
- C++
helpviewer_keywords:
- C2823
ms.assetid: 982b1b35-1a7c-456e-b711-f80cfe2d571e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 09b8284626a6af6851147dc36b67e25b76f8eb01
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46069522"
---
# <a name="compiler-error-c2823"></a>컴파일러 오류 C2823

> typedef 템플릿이 잘못 되었습니다.

서식 파일에서 허용 되지 않는 `typedef` 정의 합니다.

## <a name="example"></a>예제

다음 샘플 C2823, 생성 및이 해결 하는 방법을 보여 줍니다.

```cpp
// C2823.cpp
template<class T>
typedef struct x {
   T i;   // C2823 can't use T, specify data type and delete template
   int i;   // OK
} x1;
```