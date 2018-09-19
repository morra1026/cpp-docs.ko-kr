---
title: 컴파일러 오류 C2581 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2581
dev_langs:
- C++
helpviewer_keywords:
- C2581
ms.assetid: 24a4e4c1-24d3-4e42-b760-7dcaf9740b16
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0763db5d6284942ff3f8104eaabf705305f86e1f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46018668"
---
# <a name="compiler-error-c2581"></a>컴파일러 오류 C2581

'type': 정적 ' operator =' 함수에 유효 하지 않은

할당 (`=`) 연산자를 잘못 선언 되었습니다 `static`합니다. 할당 연산자 일 수 없습니다 `static`합니다. 자세한 내용은 [사용자 정의 연산자 (C + + /cli CLI)](../../dotnet/user-defined-operators-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플 C2581를 생성합니다.

```
// C2581.cpp
// compile with: /clr /c
ref struct Y {
   static Y ^ operator = (Y^ me, int i);   // C2581
   Y^ operator =(int i);   // OK
};
```