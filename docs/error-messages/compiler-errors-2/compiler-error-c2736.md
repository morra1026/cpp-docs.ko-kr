---
title: 컴파일러 오류 C2736 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2736
dev_langs:
- C++
helpviewer_keywords:
- C2736
ms.assetid: 95a6bc28-c0cb-49dc-87e6-e993dbbba881
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bda520c403de38481c5b84904aac5e733a90237c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049945"
---
# <a name="compiler-error-c2736"></a>컴파일러 오류 C2736

'keyword' 키워드는 캐스트를 사용할 수 없으므로

키워드는 캐스트에 올바르지 않습니다.

다음 샘플에서는 C2736를 생성합니다.

```
// C2736.cpp
int main() {
   return (virtual) 0;   // C2736
   // try the following line instead
   // return 0;
}
```