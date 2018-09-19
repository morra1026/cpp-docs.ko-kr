---
title: 컴파일러 오류 C2677 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2677
dev_langs:
- C++
helpviewer_keywords:
- C2677
ms.assetid: 76bc0b65-f52a-45a6-b6d6-0555f89da9a8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1cd7e4b3b454d8611c52bbe88041677434492c0f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46030783"
---
# <a name="compiler-error-c2677"></a>컴파일러 오류 C2677

이항 'operator': 'type' 형식을 사용 하는 전역 연산자 없습니다 (또는 허용 된 변환이)

연산자를 사용하려면 지정된 형식에 대해 오버로드하거나 연산자가 정의된 형식으로의 변환을 정의해야 합니다.

다음 샘플에서는 C2677 오류가 생성 됩니다.

```
// C2677.cpp
class C {
public:
   C(){}
} c;

class D {
public:
   D(){}
   operator int(){return 0;}
} d;

int main() {
   int i = 1 >> c;   // C2677
   int j = 1 >> d;   // OK operator int() defined
}
```