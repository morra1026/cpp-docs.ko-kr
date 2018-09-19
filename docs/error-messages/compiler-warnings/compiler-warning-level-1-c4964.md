---
title: 컴파일러 경고 (수준 1) C4964 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4964
dev_langs:
- C++
helpviewer_keywords:
- C4964
ms.assetid: b89c9274-8a92-4b7c-aa30-3fbb1b68ac73
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7f1644e4603bae36ec9d407294dea78a27e60539
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46086670"
---
# <a name="compiler-warning-level-1-c4964"></a>컴파일러 경고(수준 1) C4964

최적화 옵션을 지정 합니다. 프로필 정보 수집 되지 않습니다.

[/GL](../../build/reference/gl-whole-program-optimization.md) 하 고 [/LTCG](../../build/reference/ltcg-link-time-code-generation.md) 최적화 없음 하지만 지정 된 요청 된.pgc 파일이 생성 되 고, 따라서 없습니다 프로필 기반 최적화를 수행할 수 있도록 합니다.

응용 프로그램을 실행할 때 생성할.pgc 파일을 원한다 면 중 하나를 지정 합니다 [/O](../../build/reference/o-options-optimize-code.md) 컴파일러 옵션입니다.

다음 샘플에서는 C4964 오류가 생성 됩니다.

```
// C4964.cpp
// compile with: /W1 /GL /link /ltcg:pgi
// C4964 expected
// Add /O2, for example, to the command line to resolve this warning.
int main() {
   int i;
}
```