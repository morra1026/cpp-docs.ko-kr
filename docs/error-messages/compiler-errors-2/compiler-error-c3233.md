---
title: 컴파일러 오류 C3233 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3233
dev_langs:
- C++
helpviewer_keywords:
- C3233
ms.assetid: a9210830-1136-4f02-ba41-030c85f93547
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 87a5494e4894077d6f9dc61d920ed42db9872988
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46035450"
---
# <a name="compiler-error-c3233"></a>컴파일러 오류 C3233

'type': 제네릭 형식 매개 변수에 이미 제약 조건이 적용되었습니다.

제네릭 매개 변수를 둘 이상의 `where` 절에 포함할 수 없습니다.

다음 샘플에서는 C3233을 생성합니다.

```
// C3233.cpp
// compile with: /clr /LD

interface struct C {};
interface struct D {};

generic <class T>
where T : C
where T : D
ref class E {};   // C3233
```