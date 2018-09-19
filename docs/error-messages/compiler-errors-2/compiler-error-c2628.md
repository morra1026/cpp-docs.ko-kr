---
title: 컴파일러 오류 C2628 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2628
dev_langs:
- C++
helpviewer_keywords:
- C2628
ms.assetid: 19a25e77-d5be-4107-88d5-0745b6281f98
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 43a7d0515013158932f627b883ab36a2793ab5bd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051350"
---
# <a name="compiler-error-c2628"></a>컴파일러 오류 C2628

'type1' 'type2' 뒤에 유효 하지 않은 (했는지를 ';'?)

세미콜론 누락 될 수 있습니다.

다음 샘플에서는 C2628 오류가 생성 됩니다.

```
// C2628.cpp
class CMyClass {}
int main(){}   // C2628 error
```

해결 방법:

```
// C2628b.cpp
class CMyClass {};
int main(){}
```