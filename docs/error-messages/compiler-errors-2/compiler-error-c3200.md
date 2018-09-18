---
title: 컴파일러 오류 C3200 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3200
dev_langs:
- C++
helpviewer_keywords:
- C3200
ms.assetid: 44bb5e77-f0ec-421c-a732-b9ee7c0a3529
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 77be23b92d5237d2fa65557bdf36de31cd27d9d3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062646"
---
# <a name="compiler-error-c3200"></a>컴파일러 오류 C3200

'template': 템플릿 매개 변수 'parameter' 인수가 잘못 된 템플릿 클래스 템플릿이 필요

클래스 템플릿에 잘못 된 인수를 전달 합니다. 클래스 템플릿을에서는 템플릿 매개 변수로 사용 합니다. 다음 예에서 호출 `Y<int, int> aY` C3200를 생성 합니다. 첫 번째 매개 변수 해야 템플릿을 같은 `Y<X, int> aY`합니다.

```
// C3200.cpp
template<typename T>
class X
{
};

template<template<typename U> class T1, typename T2>
class Y
{
};

int main()
{
   Y<int, int> y;   // C3200
}
```