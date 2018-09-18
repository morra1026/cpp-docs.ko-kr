---
title: 컴파일러 오류 C2756 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2756
dev_langs:
- C++
helpviewer_keywords:
- C2756
ms.assetid: 42eb988d-4043-4dee-8fd4-596949f69a55
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 252f212f9034151bc5e77d1d2d6e64e1ee388faa
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46061216"
---
# <a name="compiler-error-c2756"></a>컴파일러 오류 C2756

'template type' : 부분 특수화에는 기본 템플릿 인수를 사용할 수 없습니다.

부분 특수화에 대한 템플릿에는 기본 인수가 포함될 수 없습니다.

다음 샘플에서는 C2756을 생성하고 해결 방법을 보여 줍니다.

```
// C2756.cpp
template <class T>
struct S {};

template <class T=int>
// try the following line instead
// template <class T>
struct S<T*> {};   // C2756
```