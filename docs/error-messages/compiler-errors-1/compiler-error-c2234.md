---
title: 컴파일러 오류 C2234 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2234
dev_langs:
- C++
helpviewer_keywords:
- C2234
ms.assetid: cfa42458-c803-4717-a017-9eca1c0cbfb0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 294ca98d1f4ce8a86e551ab17269458784992a53
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053104"
---
# <a name="compiler-error-c2234"></a>컴파일러 오류 C2234

'name': 참조 배열이 잘못 되었습니다.

없으므로 참조에 대 한 포인터, 참조 배열이 가능 하지 않습니다.

다음 샘플에서는 C2234 오류가 생성 됩니다.

```
// C2234.cpp
int main() {
   int i = 0, j = 0, k = 0, l = 0;
   int &array[4] = {i,j,k,l};   // C2234
   int array2[4] = {i,j,k,l};   // OK
}
```