---
title: 컴파일러 오류 C2055 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2055
dev_langs:
- C++
helpviewer_keywords:
- C2055
ms.assetid: 6cec79cc-6bec-443f-9897-fbf5452718c7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d6c63d79325417fbd9b1f451fb4a51f13957b4df
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46019344"
---
# <a name="compiler-error-c2055"></a>컴파일러 오류 C2055

형식 목록이 아니라 정식 매개 변수 목록이 필요합니다.

함수 정의는 정식 매개 변수 목록 대신 매개 변수 유형 목록을 포함합니다. ANSI C void 또는 줄임표가 않은 이름을 지정 하는 정식 매개 변수를 사용 하려면 (`...`).

다음 샘플에서는 C2055 오류가 생성 됩니다.

```
// C2055.c
// compile with: /c
void func(int, char) {}  // C2055
void func (int i, char c) {}   // OK
```