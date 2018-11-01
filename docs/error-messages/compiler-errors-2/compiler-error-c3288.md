---
title: 컴파일러 오류 C3288
ms.date: 11/04/2016
f1_keywords:
- C3288
helpviewer_keywords:
- C3288
ms.assetid: ed08a540-9751-46e1-9cbe-c51d6a49ffab
ms.openlocfilehash: 30a88d1047f8395fc8e3042cf2a1da88e6e5c2d3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50608418"
---
# <a name="compiler-error-c3288"></a>컴파일러 오류 C3288

'type': 핸들 형식에 대 한 역참조가 잘못 되었습니다.

컴파일러는 핸들 형식의 잘못 된 역참조를 발견 했습니다. 핸들 형식 역참조 하 고 참조를 할당할 수 있습니다. 자세한 내용은 [추적 참조 연산자](../../windows/tracking-reference-operator-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3288를 생성합니다.

```
// C3288.cpp
// compile with: /clr
ref class R {};
int main() {
   *(System::Object^) nullptr;   // C3288

// OK
   (System::Object^) nullptr;   // OK
   R^ r;
   R% pr = *r;
}
```