---
title: 컴파일러 오류 C2674 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2674
dev_langs:
- C++
helpviewer_keywords:
- C2674
ms.assetid: 7cbd70d8-d992-44d7-a5cb-dd8cf9c759d2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d1e8a3533d1f2ac7a309f89e52a03b3ff8a62dec
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46037738"
---
# <a name="compiler-error-c2674"></a>컴파일러 오류 C2674

이 컨텍스트에서 제네릭 선언은 허용 되지 않습니다.

제네릭 잘못 선언 되었습니다. 자세한 내용은 [제네릭](../../windows/generics-cpp-component-extensions.md)을 참조하세요.

## <a name="example"></a>예제

다음 샘플에서는 C2674 오류가 발생 합니다.

```
// C2674.cpp
// compile with: /clr /c
void F(generic <class T> ref class R1);   // C2674
generic <class T> ref class R2 {};   // OK
```