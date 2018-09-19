---
title: 컴파일러 오류 C3283 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3283
dev_langs:
- C++
helpviewer_keywords:
- C3283
ms.assetid: c51d912c-cde3-4928-904e-26734c8954ce
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0feaad0e0eb1b9dc5ee6c5b2f47e8f2a425b6d99
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46096472"
---
# <a name="compiler-error-c3283"></a>컴파일러 오류 C3283

'type': 인터페이스에는 인스턴스 생성자를 사용할 수 없습니다.

CLR [인터페이스](../../windows/interface-class-cpp-component-extensions.md) 에는 인스턴스 생성자를 사용할 수 없습니다.  정적 생성자는 허용됩니다.

다음 샘플에서는 C3283을 생성합니다.

```
// C3283.cpp
// compile with: /clr
interface class I {
   I();   // C3283
};
```

해결 방법:

```
// C3283b.cpp
// compile with: /clr /c
interface class I {
   static I(){}
};
```