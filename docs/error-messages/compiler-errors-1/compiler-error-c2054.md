---
title: 컴파일러 오류 C2054 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2054
dev_langs:
- C++
helpviewer_keywords:
- C2054
ms.assetid: 37f7c612-0d7d-4728-9e67-ac4160555f48
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5fc936bf6c42144a55bc6d84a8434959383e7e9f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46071434"
---
# <a name="compiler-error-c2054"></a>컴파일러 오류 C2054

예상 ' (' 'identifier'를 수행 합니다.

함수 식별자는 닫는 괄호가 필요한 컨텍스트에서 사용 됩니다.

이 오류는 복잡 한 초기화에 등호 (=)를 생략 하 여 발생할 수 있습니다.

다음 샘플에서는 C2054를 생성합니다.

```
// C2054.c
int array1[] { 1, 2, 3 };   // C2054, missing =
```

해결 방법:

```
// C2054b.c
int main() {
   int array2[] = { 1, 2, 3 };
}
```