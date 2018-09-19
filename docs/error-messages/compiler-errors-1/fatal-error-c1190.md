---
title: 심각한 오류 C1190 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1190
dev_langs:
- C++
helpviewer_keywords:
- C1190
ms.assetid: dee2266d-6c40-4f6e-91db-f01e65f8d2bc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 96e1ab464199466a5df13362f40ac9143be49a68
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46084954"
---
# <a name="fatal-error-c1190"></a>심각한 오류 C1190

관리되는 대상 코드에는 '/clr' 옵션을 사용해야 합니다.

CLR 구문을 사용하지만 **/clr**을 지정하지 않았습니다.

자세한 내용은 [/clr (Common Language Runtime Compilation)](../../build/reference/clr-common-language-runtime-compilation.md)을 참조하세요.

다음 샘플에서는 C1190을 생성합니다.

```
// C1190.cpp
// compile with: /c
__gc class A {};   // C1190
ref class A {};
```