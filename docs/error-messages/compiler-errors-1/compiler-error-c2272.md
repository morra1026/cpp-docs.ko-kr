---
title: 컴파일러 오류 C2272 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2272
dev_langs:
- C++
helpviewer_keywords:
- C2272
ms.assetid: 1517706a-9c27-452e-9b10-3424b3d232bc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e17765ee0acbf20d76e631bf7fccfb3413c5dc1d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46040312"
---
# <a name="compiler-error-c2272"></a>컴파일러 오류 C2272

'function': 정적 멤버 함수에서 허용 되지 않습니다 한정자

A `static` 멤버 함수는 메모리 내 모델 지정자를 사용 하 여 같은 선언 [const](../../cpp/const-cpp.md) 또는 [volatile](../../cpp/volatile-cpp.md)에서 이러한 한정자는 허용 되지 않습니다 `static` 멤버 함수입니다.

다음 샘플에서는 C2272 오류가 생성 됩니다.

```
// C2272.cpp
// compile with: /c
class CMyClass {
public:
   static void func1() const volatile;   // C2272  func1 is static
   void func2() const volatile;   // OK
};
```