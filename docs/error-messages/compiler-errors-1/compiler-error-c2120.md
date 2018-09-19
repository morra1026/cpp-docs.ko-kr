---
title: 컴파일러 오류 C2120 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2120
dev_langs:
- C++
helpviewer_keywords:
- C2120
ms.assetid: b0f3f66c-6cd2-4f48-9ea3-c270b53c2b8c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d4f4247d8e752e71b86829ea61756f2f04d26762
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46105999"
---
# <a name="compiler-error-c2120"></a>컴파일러 오류 C2120

' void' 형식도 사용할 수 없습니다.

`void` 형식은 다른 형식의 선언에 사용 됩니다.

다음 샘플에서는 C2120 오류가 생성 됩니다.

```
// C2120.cpp
int main() {
   void int i;   // C2120
   int j;   // OK
}
```