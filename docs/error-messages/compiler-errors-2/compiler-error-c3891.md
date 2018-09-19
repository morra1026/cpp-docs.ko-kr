---
title: 컴파일러 오류 C3891 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3891
dev_langs:
- C++
helpviewer_keywords:
- C3891
ms.assetid: 6e1a9458-97f5-4580-bc0f-aa97a1bfd20d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c85e5fa5ed5e6f202750fef05ffc96e9a0c86bc1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051700"
---
# <a name="compiler-error-c3891"></a>컴파일러 오류 C3891

'var': 리터럴 데이터 멤버는 l-value로 사용할 수 없습니다

A [리터럴](../../windows/literal-cpp-component-extensions.md) 변수는 const 및 선언에서 초기화 한 후 해당 값을 변경할 수 없습니다.

다음 샘플에서는 C3891 오류가 생성 됩니다.

```
// C3891.cpp
// compile with: /clr
ref struct Y1 {
   literal int staticConst = 9;
};

int main() {
   Y1::staticConst = 0;   // C3891
}
```