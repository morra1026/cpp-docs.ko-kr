---
title: 컴파일러 오류 C3181 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3181
dev_langs:
- C++
helpviewer_keywords:
- C3181
ms.assetid: 5d450f8b-6cef-4452-a0c4-2076e967451d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 599fe0afe4bdcdc7b1e2025859d11a38618b1349
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46097343"
---
# <a name="compiler-error-c3181"></a>컴파일러 오류 C3181

'type': 잘못 된 연산자의 피연산자

에 전달 된 잘못 된 매개 변수를 [typeid](../../windows/typeid-cpp-component-extensions.md) 연산자입니다. 매개 변수는 관리 되는 형식 이어야 합니다.

컴파일러에서 공용 언어 런타임 형식에 매핑되는 네이티브 형식에 대 한 별칭을 사용 하는 참고 합니다.

다음 샘플에서는 C3181 오류가 생성 됩니다.

```
// C3181a.cpp
// compile with: /clr
using namespace System;

int main() {
   Type ^pType1 = interior_ptr<int>::typeid;   // C3181
   Type ^pType2 = int::typeid;   // OK
}
```
