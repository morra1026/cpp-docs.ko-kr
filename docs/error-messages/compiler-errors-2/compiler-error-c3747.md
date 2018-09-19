---
title: 컴파일러 오류 C3747 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3747
dev_langs:
- C++
helpviewer_keywords:
- C3747
ms.assetid: a9a4be67-5d9c-4dcc-9ae9-baae46cbecde
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f1f657e6d3f64a4d8a2244ab2927a9a712c14b1a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46091675"
---
# <a name="compiler-error-c3747"></a>컴파일러 오류 C3747

기본 형식 매개 변수가 없습니다: 매개 변수 매개 변수

기본값이 있는 제네릭 또는 템플릿 매개 변수에 기본값이 없는 매개 변수에 따라 매개 변수 목록에서 올 수 없습니다.

다음 샘플에서는 C3747를 생성합니다.

```
// C3747.cpp
template <class T1 = int, class T2>   // C3747
struct MyStruct {};
```

해결 방법:

```
// C3747b.cpp
// compile with: /c
template <class T1, class T2 = int>
struct MyStruct {};
```