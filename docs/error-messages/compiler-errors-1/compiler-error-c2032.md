---
title: 컴파일러 오류 C2032 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2032
dev_langs:
- C++
helpviewer_keywords:
- C2032
ms.assetid: 625d7c83-70b6-42c2-a558-81fbc0026324
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6ab02ca695ec94f25054e3490232b782a46a53a4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064011"
---
# <a name="compiler-error-c2032"></a>컴파일러 오류 C2032

'identifier': 함수는 'structorunion' 구조체/공용 구조체의 멤버일 수 없습니다

구조체 또는 공용 구조체에 3. 아니라 c + +에서 허용 되는 멤버 함수 오류를 해결 하려면 c + + 프로그램 컴파일 또는 멤버 함수를 제거 합니다.

다음 샘플에서는 C2032 오류가 생성 됩니다.

```
// C2032.c
struct z {
   int i;
   void func();   // C2032
};
```

해결 방법:

```
// C2032b.c
// compile with: /c
struct z {
   int i;
};
```