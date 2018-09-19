---
title: 컴파일러 오류 C2499 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2499
dev_langs:
- C++
helpviewer_keywords:
- C2499
ms.assetid: b323ff4d-b3c1-4bfd-b052-ae7292d53222
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 27f10cc2f48a72222a6e9a2a7187ba9a1f6fb450
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46043952"
---
# <a name="compiler-error-c2499"></a>컴파일러 오류 C2499

'class': 클래스는 자체 기본 클래스일 수 없습니다

기본 클래스로 정의 하는 클래스를 지정 하려고 했습니다.

다음 샘플에서는 C2499 오류가 생성 됩니다.

```
// C2499.cpp
// compile with: /c
class CMyClass : public CMyClass {};   // C2499
class CMyClass{};   // OK
```