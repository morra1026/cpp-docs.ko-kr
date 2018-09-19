---
title: 컴파일러 오류 C3913 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3913
dev_langs:
- C++
helpviewer_keywords:
- C3913
ms.assetid: a678bfce-9524-470d-9f23-7d08ecb972c8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f9b2ad0cc6bda9f46e3cf0a65de9e41b1808ac1f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46098801"
---
# <a name="compiler-error-c3913"></a>컴파일러 오류 C3913

기본 속성 인덱싱되어 야 합니다.

기본 속성을 잘못 정의 되었습니다.

자세한 내용은 [property](../../windows/property-cpp-component-extensions.md)을 참조하세요.

다음 샘플에서는 C3913 오류가 생성 됩니다.

```
// C3913.cpp
// compile with: /clr /c
ref struct X {
   property int default {   // C3913
   // try the following line instead
   // property int default[int] {
      int get(int) { return 0; }
      void set(int, int) {}
   }
};
```