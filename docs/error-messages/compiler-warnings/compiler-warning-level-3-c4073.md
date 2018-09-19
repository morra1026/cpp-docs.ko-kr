---
title: 컴파일러 경고 (수준 3) C4073 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4073
dev_langs:
- C++
helpviewer_keywords:
- C4073
ms.assetid: 50081a6e-6acd-45ff-8484-9b1ea926cc5c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 24af5c41a524b4178f1402008203959c4e6b021d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46088620"
---
# <a name="compiler-warning-level-3-c4073"></a>컴파일러 경고 (수준 3) C4073

이니셜라이저가 라이브러리 초기화 영역

타사 라이브러리 개발자에 의해 지정 되는 라이브러리 초기화 영역을 사용 해야 하는 전용 [#pragma init_seg](../../preprocessor/init-seg.md)합니다. 다음 샘플에서는 C4073 오류가 생성 됩니다.

```
// C4073.cpp
// compile with: /W3
#pragma init_seg(lib)   // C4073

// try this line to resolve the warning
// #pragma init_seg(user)

int main() {
}
```