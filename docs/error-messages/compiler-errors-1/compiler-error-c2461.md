---
title: 컴파일러 오류 C2461 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2461
dev_langs:
- C++
helpviewer_keywords:
- C2461
ms.assetid: e64ba651-f441-4fdb-b5cb-4209bbbe4db4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 39d58b315fdd7e3c4e1899041cebf8400813ed40
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46029301"
---
# <a name="compiler-error-c2461"></a>컴파일러 오류 C2461

> '*클래스*': 생성자 구문에 정식 매개 변수가 없음

클래스의 생성자는 정식 매개 변수를 지정 하지 않습니다. 생성자 선언에 정식 매개 변수 목록을 지정 해야 합니다. 목록은 비어 있을 수 있습니다.

이 문제를 해결 하려면 선언 뒤에 괄호 한 쌍 추가 *클래스*:: **클래스*합니다.

## <a name="example"></a>예제

다음 샘플 C2461를 해결 하는 방법을 보여 줍니다.

```cpp
// C2461.cpp
// compile with: /c
class C {
   C::C;     // C2461
   C::C();   // OK
};
```