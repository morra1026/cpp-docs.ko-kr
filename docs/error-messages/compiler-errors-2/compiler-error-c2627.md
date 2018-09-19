---
title: 컴파일러 오류 C2627 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2627
dev_langs:
- C++
helpviewer_keywords:
- C2627
ms.assetid: 7fc6c5ac-c7c9-4f0b-ad52-f52252526458
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a7548e2154144ca502ab581bf804018b80cc0d8d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46072669"
---
# <a name="compiler-error-c2627"></a>컴파일러 오류 C2627

'function': 멤버 함수를 익명 공용 구조체에 사용할 수 없습니다

[익명 공용 구조체](../../cpp/unions.md#anonymous_unions) 멤버 함수를 사용할 수 없습니다.

다음 샘플에서는 C2627 오류가 생성 됩니다.

```
// C2627.cpp
int main() {
   union { void f(){} };   // C2627
   union X { void f(){} };
}
```