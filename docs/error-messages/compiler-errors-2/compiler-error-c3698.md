---
title: 컴파일러 오류 C3698 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3698
dev_langs:
- C++
helpviewer_keywords:
- C3698
ms.assetid: 3c02fb08-7ba4-4637-a06f-19926cb2b5f1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e9ca53e5b614b5e1d85832a7ad437a39ac1c5d87
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46107901"
---
# <a name="compiler-error-c3698"></a>컴파일러 오류 C3698

'type': 'operator'의 인수로이 형식을 사용할 수 없습니다

관리 되는 개체를 올바르게 선언 되었습니다.

다음 샘플에서는 C3698를 생성합니다.

```
// C3698.cpp
// compile with: /clr

int main() {
   array<int>^a = new array<int>^(20);   // C3698
   array<int>^a2 = gcnew array<int>(20);   // OK
}
```