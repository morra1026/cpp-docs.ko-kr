---
title: 컴파일러 경고 (수준 3) C4633 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4633
dev_langs:
- C++
helpviewer_keywords:
- C4633
ms.assetid: 6d76f268-ba8c-448b-8e83-b903a18b583b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 54a180bcd135f4614fa6cc67cf7647acdfa1c445
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085747"
---
# <a name="compiler-warning-level-3-c4633"></a>컴파일러 경고(수준 3) C4633

XML 문서 주석 대상: 오류: 이유

이름을 전달 합니다 [ \<매개 변수 >](../../ide/param-visual-cpp.md) 컴파일러에서 태그를 찾을 수 없습니다.

다음 샘플에서는 C4633 오류가 생성 됩니다.

```
// C4633.cpp
// compile with: /clr /doc /LD /W3

/// Text for class MyClass.
public ref class MyClass {
   // C4633 remove line for Int3
   /// <param name="Int1">Used to indicate status.</param>
   /// <param name="Int3">Used to indicate status.</param>
   void MyMethod(int Int1) {
      Int1 = 0;
      Int1++;
   }
};
```