---
title: 컴파일러 오류 C2541 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2541
dev_langs:
- C++
helpviewer_keywords:
- C2541
ms.assetid: ed95180f-00df-4e62-a8e9-1b6dab8281bf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 492f6f938af5e09221bff3c1c848c9688b28931d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049152"
---
# <a name="compiler-error-c2541"></a>컴파일러 오류 C2541

'delete': 삭제: 포인터가 아닌 개체를 삭제할 수 없습니다

합니다 [삭제](../../cpp/delete-operator-cpp.md) 연산자가 포인터가 아닌 개체에 사용 되었습니다.

다음 샘플에서는 C2541 오류가 생성 됩니다.

```
// C2541.cpp
int main() {
   int i;
   delete i;   // C2541 i not a pointer

   // OK
   int *ip = new int;
   delete ip;
}
```