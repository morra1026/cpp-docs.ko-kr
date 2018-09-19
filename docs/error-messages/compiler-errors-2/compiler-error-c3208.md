---
title: 컴파일러 오류 C3208 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3208
dev_langs:
- C++
helpviewer_keywords:
- C3208
ms.assetid: 6d060bfe-52cf-4599-8f70-bdeb5a670df3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 53564517eaed44c21e6eccb58ad6399788129687
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078506"
---
# <a name="compiler-error-c3208"></a>컴파일러 오류 C3208

'function': 클래스 템플릿 'class'에 대한 템플릿 매개 변수 목록이 template 템플릿 매개 변수 'parameter'에 대한 템플릿 매개 변수 목록과 일치하지 않습니다.

template 템플릿 매개 변수의 템플릿 매개 변수 개수가 제공된 클래스 템플릿과 다릅니다.

다음 샘플에서는 C3208을 생성합니다.

```
// C3208.cpp
template <template <class T> class TT >
int f();

template <class T1, class T2>
struct S;

template <class T1>
struct R;

int i = f<S>();   // C3208
// try the following line instead
// int i = f<R>();
```