---
title: 컴파일러 오류 C2760 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2760
dev_langs:
- C++
helpviewer_keywords:
- C2760
ms.assetid: 585757fd-d519-43f3-94e5-50316ac8b90b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9ae920b9bf0d6d8a743bd9defac883304e80c117
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026090"
---
# <a name="compiler-error-c2760"></a>컴파일러 오류 C2760

구문 오류: 'name1'가 필요 하지 'name2'

캐스팅 연산자에 잘못 된 연산자를 사용 하 여 사용 됩니다.

다음 샘플에서는 C2760 오류가 생성 됩니다.

```
// C2760.cpp
class B {};
class D : public B {};

void f(B* pb) {
    D* pd1 = static_cast<D*>(pb);
    D* pd2 = static_cast<D*>=(pb);  // C2760
    D* pd3 = static_cast<D*=(pb);   // C2760
}
```