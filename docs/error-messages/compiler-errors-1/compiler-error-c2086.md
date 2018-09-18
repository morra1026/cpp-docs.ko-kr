---
title: 컴파일러 오류 C2086 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2086
dev_langs:
- C++
helpviewer_keywords:
- C2086
ms.assetid: 4329bf72-90c8-444c-8524-4ef75e6b2139
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d0e0d8b105d58b0585bc31b8d340d3d7ba5fb29e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46029847"
---
# <a name="compiler-error-c2086"></a>컴파일러 오류 C2086

'identifier': 재정의

식별자가 두 번 이상 정의 또는 후속 선언 이전에서 다릅니다.

C2086 참조 된 C# 어셈블리에 대 한 증분 빌드 결과일 수도 있습니다. 이 오류를 해결 하려면 C# 어셈블리를 다시 작성 합니다.

다음 샘플에서는 C2086를 생성합니다.

```
// C2086.cpp
main() {
  int a;
  int a;   // C2086 not an error in ANSI C
}
```