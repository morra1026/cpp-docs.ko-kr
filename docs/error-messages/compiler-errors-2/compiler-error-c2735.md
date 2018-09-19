---
title: 컴파일러 오류 C2735 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2735
dev_langs:
- C++
helpviewer_keywords:
- C2735
ms.assetid: 6ce45600-7148-4bc0-8699-af0ef137571e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 732b75c8988f879af230e0513a751b8cd9c4ae67
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46093127"
---
# <a name="compiler-error-c2735"></a>컴파일러 오류 C2735

정식 매개 변수 형식 지정자에는 'keyword' 키워드를 사용할 수 없습니다.

키워드가이 컨텍스트에서 올바르지 않습니다.

다음 샘플에서는 C2735 오류가 생성 됩니다.

```
// C2735.cpp
void f(inline int){}   // C2735
```