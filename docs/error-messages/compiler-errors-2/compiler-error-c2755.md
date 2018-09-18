---
title: 컴파일러 오류 C2755 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2755
dev_langs:
- C++
helpviewer_keywords:
- C2755
ms.assetid: 8ee4eeb6-4757-4efe-9100-38ff4a96f1de
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 56ecf997df2aeb1a41b5021d61b24073e871b55f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064918"
---
# <a name="compiler-error-c2755"></a>컴파일러 오류 C2755

'param': 부분 특수화의 비형식 매개 변수는 단순 식별자 여야 합니다.

비형식 매개 변수는 단순 식별자를 컴파일러가 컴파일 시간에 단일 식별자 또는 상수 값을 확인할 수 있어야 합니다.

다음 샘플에서는 C2755 오류가 생성 됩니다.

```
// C2755.cpp
template<int I, int J>
struct A {};

template<int I>
struct A<I,I*5> {};   // C2755
// try the following line instead
// struct A<I,5> {};
```