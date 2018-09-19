---
title: 컴파일러 오류 C2438 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2438
dev_langs:
- C++
helpviewer_keywords:
- C2438
ms.assetid: 3a0ab3ba-d0e4-4d8f-971d-e503397cc827
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4f5153e3ff6626f3ea1b1155f14bc9ef96441e7d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46066078"
---
# <a name="compiler-error-c2438"></a>컴파일러 오류 C2438

'identifier': 생성자를 통해 정적 클래스 데이터를 초기화할 수 없습니다

생성자는 클래스의 정적 멤버 초기화에 사용 됩니다. 정적 멤버는 클래스 선언 밖에 정의에서 초기화 되어야 합니다.

다음 샘플에서는 C2438를 생성합니다.

```
// C2438.cpp
struct X {
   X(int i) : j(i) {}   // C2438
   static int j;
};

int X::j;

int main() {
   X::j = 1;
}
```