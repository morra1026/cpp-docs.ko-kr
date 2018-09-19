---
title: 컴파일러 오류 C2838 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2838
dev_langs:
- C++
helpviewer_keywords:
- C2838
ms.assetid: 176b2ad6-7a84-4019-b97e-328866054457
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c5607df86a44174536f58242c5c0a98f7fe5e7dc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045278"
---
# <a name="compiler-error-c2838"></a>컴파일러 오류 C2838

'member': 멤버 선언의 정규화 된 이름이 잘못 되었습니다.

클래스, 구조체 또는 공용 구조체에는 다른 클래스, 구조체 또는 공용 구조체의 멤버를 다시 선언 정규화 된 이름을 사용 합니다.

다음 샘플에서는 C2838 오류가 생성 됩니다.

```
// C2838.cpp
// compile with: /c
class Bellini {
public:
    void Norma();
};

class Bottesini {
   Bellini::Norma();  // C2838
};
```