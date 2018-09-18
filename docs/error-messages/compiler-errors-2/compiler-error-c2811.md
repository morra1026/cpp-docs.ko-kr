---
title: 컴파일러 오류 C2811 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2811
dev_langs:
- C++
helpviewer_keywords:
- C2811
ms.assetid: 6a44b18e-44c1-49d8-9b99-e0545b9a6e7d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e7e3b2d7bb76989b2028846efee6b18d10e1b0ad
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46059617"
---
# <a name="compiler-error-c2811"></a>컴파일러 오류 C2811

'type1': ref 'type2'에서 상속할 수 없습니다. 클래스는 ref 클래스 또는 인터페이스 클래스 에서만 상속할 수

관리 되지 않는 클래스를 관리 되는 클래스에 대 한 기본 클래스로 사용 하려고 했습니다.

다음 샘플에서는 C2811 오류가 생성 됩니다.

```
// C2811.cpp
// compile with: /clr /c
struct S{};
ref struct T {};
ref class C : public S {};   // C2811
ref class D : public T {};   // OK
```