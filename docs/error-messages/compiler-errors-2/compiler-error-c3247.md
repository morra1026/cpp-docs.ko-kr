---
title: 컴파일러 오류 C3247
ms.date: 11/04/2016
f1_keywords:
- C3247
helpviewer_keywords:
- C3247
ms.assetid: f9a2bbb5-3fce-40bf-9fd3-835a5f164dbb
ms.openlocfilehash: 7ca84b4f054852aefa75a9c4547286137b436c63
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50569167"
---
# <a name="compiler-error-c3247"></a>컴파일러 오류 C3247

'class1': coclass는 다른 coclass 'class2'에서 상속할 수 없습니다.

[coclass](../../windows/coclass.md) 특성으로 표시된 클래스는 `coclass` 특성으로 표시된 다른 클래스에서 상속할 수 없습니다.

다음 샘플에서는 C3247을 생성합니다.

```
// C3247.cpp
[module(name="MyLib")];
[coclass]
class a {
};

[coclass]
class b : public a {   // C3247
};
int main() {
}
```