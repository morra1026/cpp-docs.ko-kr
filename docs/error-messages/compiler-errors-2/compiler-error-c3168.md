---
title: 컴파일러 오류 C3168 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3168
dev_langs:
- C++
helpviewer_keywords:
- C3168
ms.assetid: 4c36fcfb-c351-48ff-b4eb-78d2aa1b4d55
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b2a70af70af5b31ef9a3bf2fe939eef28783369a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46106456"
---
# <a name="compiler-error-c3168"></a>컴파일러 오류 C3168

'type': 열거형의 내부 형식이 잘못 되었습니다.

에 지정 된 형식의 기본는 `enum` 유형이 잘못 되었습니다. C + + 정수 형식 또는 해당 CLR 형식이 기본 형식 이어야 합니다.

다음 샘플에서는 C3168를 생성합니다.

```
// C3168.cpp
// compile with: /clr /c
ref class G{};

enum class E : G { e };   // C3168
enum class F { f };   // OK
```
