---
title: 컴파일러 오류 C3883 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3883
dev_langs:
- C++
helpviewer_keywords:
- C3883
ms.assetid: cdd1c1f4-f268-4469-9c62-d52303114b0c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4387eacb4e35c82af5c2617771b8c887dae42c4e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045473"
---
# <a name="compiler-error-c3883"></a>컴파일러 오류 C3883

'var': initonly 정적 데이터 멤버를 초기화 해야 합니다

변수 표시 [initonly](../../dotnet/initonly-cpp-cli.md) 올바르게 초기화 되지 않았습니다.

다음 샘플에서는 C3883 오류가 생성 됩니다.

```
// C3883.cpp
// compile with: /clr
ref struct Y1 {
   initonly
   static int staticConst1;   // C3883
};
```

다음 샘플에는 가능한 해결 방법을 보여 줍니다.

```
// C3883b.cpp
// compile with: /clr /c
ref struct Y1 {
   initonly
   static int staticConst2 = 0;
};
```

다음 샘플에는 정적 생성자에서 초기화 하는 방법을 보여 줍니다.

```
// C3883c.cpp
// compile with: /clr /LD
ref struct Y1 {
   initonly
   static int staticConst1;

   static Y1() {
      staticConst1 = 0;
   }
};
```