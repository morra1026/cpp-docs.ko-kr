---
title: 컴파일러 오류 C2959
ms.date: 11/04/2016
f1_keywords:
- C2959
helpviewer_keywords:
- C2959
ms.assetid: d66bb2a8-70c3-4209-a358-b0c47f111a50
ms.openlocfilehash: c45466fdf8d0c4bec67779943a5868299f05cf79
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50535735"
---
# <a name="compiler-error-c2959"></a>컴파일러 오류 C2959

제네릭 클래스 또는 함수 템플릿의 구성원이 아닐 수 있습니다.

자세한 내용은 [Windows 런타임 및 관리 템플릿](../../windows/windows-runtime-and-managed-templates-cpp-component-extensions.md) 하 고 [제네릭](../../windows/generics-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C2959를 생성합니다.

```
// C2959.cpp
// compile with: /clr /c
template <class T> ref struct S {
   generic <class U> ref struct GR1;   // C2959
};
```