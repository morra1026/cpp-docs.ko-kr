---
title: 컴파일러 오류 C3174
ms.date: 11/04/2016
f1_keywords:
- C3174
helpviewer_keywords:
- C3174
ms.assetid: fe6b3b5a-8196-485f-a45f-0b2e51df4086
ms.openlocfilehash: 32f39eb1d808ccedd27ae3e4d343b87ddfde1862
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50666351"
---
# <a name="compiler-error-c3174"></a>컴파일러 오류 C3174

모듈 특성을 지정 하지 않았습니다.

Visual c + + 특성을 사용 하는 프로그램을 사용 하지 않았습니다 합니다 [모듈](../../windows/module-cpp.md) 특성을 사용 하는 프로그램에 필요한 특성입니다.

다음 샘플에서는 C3174 오류가 생성 됩니다.

```
// C3174.cpp
// C3174 expected
// uncomment the following line to resolve this C3174
// [module(name="x")];
[export]
struct S
{
   int i;
};

int main()
{
}
```