---
title: 컴파일러 오류 C2206 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2206
dev_langs:
- C++
helpviewer_keywords:
- C2206
ms.assetid: d7fba68b-aa28-4885-a9a0-27107358f066
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 82f1599b927e04f2f9196229bf7c8aaf5e49c13f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46060059"
---
# <a name="compiler-error-c2206"></a>컴파일러 오류 C2206

'function': 형식 정의는 함수 정의에 사용할 수 없습니다.

`typedef` 가 함수 형식을 정의하는 데 사용됩니다.

다음 샘플에서는 C2206을 생성합니다.

```
// C2206.cpp
typedef int functyp();
typedef int MyInt;
functyp func1 {};   // C2206
int main() {
   MyInt i = 0;   // OK
}
```