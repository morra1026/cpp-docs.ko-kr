---
title: 컴파일러 오류 C2005 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2005
dev_langs:
- C++
helpviewer_keywords:
- C2005
ms.assetid: 090530ed-e0ec-4358-833a-ca24260e7ffe
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a6dfba3b960a046bf40751c135c3b99fbe843545
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46100682"
---
# <a name="compiler-error-c2005"></a>컴파일러 오류 C2005

\#줄 'token' 찾을 줄 번호 필요

`#line` 지시문 뒤에 줄 번호와 합니다.

다음 샘플에서는 C2005 오류가 생성 됩니다.

```
// C2005.cpp
int main() {
   int i = 0;
   #line i   // C2005
}
```

해결 방법:

```
// C2005b.cpp
int main() {
   int i = 0;
   #line 0
}
```