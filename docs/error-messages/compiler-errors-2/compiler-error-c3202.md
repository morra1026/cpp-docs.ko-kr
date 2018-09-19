---
title: 컴파일러 오류 C3202 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3202
dev_langs:
- C++
helpviewer_keywords:
- C3202
ms.assetid: 23528a0c-5493-4804-9789-cd3c38e49fb9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 254843386943b677be6df2c1ab7f1da56265e1d8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070327"
---
# <a name="compiler-error-c3202"></a>컴파일러 오류 C3202

'arg name' : 템플릿 매개 변수 'parameter'에 대한 기본 인수가 잘못되었습니다. 클래스 템플릿이 필요합니다.

템플릿 매개 변수에 대해 잘못된 기본 인수를 전달했습니다.

다음 샘플에서는 C3202를 생성합니다.

```
// C3202.cpp
template<typename T>
class X
{
};

class Z
{
};

template<template<typename U> class T1 = Z, typename T2> // C3202
class Y
{
};
```