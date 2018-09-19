---
title: 컴파일러 오류 C2142 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2142
dev_langs:
- C++
helpviewer_keywords:
- C2142
ms.assetid: d0dbe10e-0952-49a4-8b33-e82fb7558b19
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 32301087ac1f06f1958ca8de7d2f66645dafb3d2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032501"
---
# <a name="compiler-error-c2142"></a>컴파일러 오류 C2142

함수 선언이 서로 다릅니다. 그 중 하나에 지정 하는 가변 매개 변수

하나의 함수 선언에 가변 매개 변수 목록을 포함합니다. 다른 선언 되지 않습니다. ANSI C ([/Za](../../build/reference/za-ze-disable-language-extensions.md))만 합니다.

다음 샘플에서는 C2142 오류가 생성 됩니다.

```
// C2142.c
// compile with: /Za /c
void func();
void func( int, ... );   // C2142
void func2( int, ... );   // OK
```