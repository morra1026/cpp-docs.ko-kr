---
title: 컴파일러 오류 C2675 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2675
dev_langs:
- C++
helpviewer_keywords:
- C2675
ms.assetid: 4b92a12b-bff8-4dd5-a109-620065fc146c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1772f6e88516e7c8c1498f84d180ab6c4e0e05ab
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46102407"
---
# <a name="compiler-error-c2675"></a>컴파일러 오류 C2675

단항 'operator': 'type' 정의 하지 않습니다이 연산자 또는 허용 되는 형식으로의 변환을 미리 정의 된 운영자에 게

단항 연산자를 사용 하는 경우에 C2675 발생할 수 있습니다 및 형식을 정의 하지 않습니다는 operator 또는 허용 되는 형식으로의 변환을 미리 정의 된 운영자에 게 합니다. 연산자를 사용하려면 지정된 형식에 대해 오버로드하거나 연산자가 정의된 형식으로의 변환을 정의해야 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2675 오류가 발생 합니다.

```
// C2675.cpp
struct C {
   C(){}
} c;

struct D {
   D(){}
   void operator-(){}
} d;

int main() {
   -c;   // C2675
   -d;   // OK
}
```