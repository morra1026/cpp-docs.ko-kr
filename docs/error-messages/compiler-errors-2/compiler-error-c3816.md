---
title: 컴파일러 오류 C3816 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3816
dev_langs:
- C++
helpviewer_keywords:
- C3816
ms.assetid: 2e52cc7f-e31c-41a3-8d6f-9f5fab3648c0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bfc0cf864caeefd5b19e3d40383724909575d4df
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46115895"
---
# <a name="compiler-error-c3816"></a>컴파일러 오류 C3816

'declaration' 이전에 선언 되었거나 다른 관리 되는 또는 WinRTmodifier 정의

정방향 선언 및 실제 선언에서는 특성의 선언에 충돌이나 불일치가 없어야 합니다.

다음 샘플에서는 C3816을 생성하고 해결 방법을 보여 줍니다.

```
// C3816a.cpp
// compile with: /clr /c
class C1;
// try the following line instead
// ref class C1;

ref class C1{  // C3816, forward declaration does not use ref
};
```