---
title: 컴파일러 오류 C2673 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2673
dev_langs:
- C++
helpviewer_keywords:
- C2673
ms.assetid: 780230c0-619b-4a78-b01d-ff5886306741
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 942ad581c4b272078eabfe225e7fdab2245d0ad2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46108529"
---
# <a name="compiler-error-c2673"></a>컴파일러 오류 C2673

'function': 전역 함수에 'this' 포인터가 없습니다.

전역 함수에 액세스 하려고 `this`합니다.

다음 샘플에서는 C2673 오류가 생성 됩니다.

```
// C2673.cpp
int main() {
   this = 0;   // C2673
}
```