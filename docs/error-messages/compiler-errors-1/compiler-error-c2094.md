---
title: 컴파일러 오류 C2094 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2094
dev_langs:
- C++
helpviewer_keywords:
- C2094
ms.assetid: 9e4f8f88-f189-46e7-91c9-481bacc7af87
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6e3591fef423bc24562a2f2edf18f7f2774cfcc4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46073527"
---
# <a name="compiler-error-c2094"></a>컴파일러 오류 C2094

'identifier' 레이블이 정의되지 않았습니다.

[goto](../../cpp/goto-statement-cpp.md) 문에서 사용하는 레이블이 함수에 존재하지 않습니다.

## <a name="example"></a>예제

다음 샘플에서는 C2094를 생성합니다.

```cpp
// C2094.c
int main() {
   goto test;
}   // C2094
```

해결 방법:

```cpp
// C2094b.c
int main() {
   goto test;
   test:
   {
   }
}
```