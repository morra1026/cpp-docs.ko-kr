---
title: 컴파일러 오류 C2467 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2467
dev_langs:
- C++
helpviewer_keywords:
- C2467
ms.assetid: f9ead270-5d0b-41cc-bdcd-586a647c67a7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8bab320bfdba9fcbd408771b7859a22fc85fa06e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46048777"
---
# <a name="compiler-error-c2467"></a>컴파일러 오류 C2467

익명 ' 사용자 정의 형식당 ' 선언은 올바르지 않습니다

중첩 된 사용자 정의 형식 선언 되었습니다. ANSI 호환성 옵션을 사용 하 여 C 소스 코드를 컴파일할 때 오류입니다 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) 사용 하도록 설정 합니다.

다음 샘플에서는 C2467 오류가 생성 됩니다.

```
//C2467.c
// compile with: /Za
int main() {
   struct X {
      union { int i; };   // C2467, nested declaration
   };
}
```