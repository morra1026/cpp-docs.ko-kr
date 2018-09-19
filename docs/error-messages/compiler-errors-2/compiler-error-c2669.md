---
title: 컴파일러 오류 C2669 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2669
dev_langs:
- C++
helpviewer_keywords:
- C2669
ms.assetid: f9cb8111-bcdc-484b-a863-2c42e15a0496
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 04363816e69dd560acc0497128f13d92c9878005
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46050699"
---
# <a name="compiler-error-c2669"></a>컴파일러 오류 C2669

멤버 함수를 익명 공용 구조체에 사용할 수 없습니다

[익명 공용 구조체](../../cpp/unions.md#anonymous_unions) 멤버 함수를 사용할 수 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C2669 오류가 생성 됩니다.

```cpp
// C2669.cpp
struct X {
   union {
      int i;
      void f() {   // C2669, remove function
         i = 0;
      }
   };
};
```
