---
title: 컴파일러 오류 C3282 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3282
dev_langs:
- C++
helpviewer_keywords:
- C3282
ms.assetid: bac2ac89-c360-4c24-bb81-c20c62ece9ba
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: da6d4fd30d109f78949a3ec53e0d46d6a9de7dc9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46056900"
---
# <a name="compiler-error-c3282"></a>컴파일러 오류 C3282

관리 되는 제네릭 매개 변수 목록에만 나타날 수 있습니다 또는 WinRTclasses, 구조체 또는 함수

제네릭 매개 변수 목록이 잘못 사용되었습니다.  자세한 내용은 [제네릭](../../windows/generics-cpp-component-extensions.md)을 참조하세요.

## <a name="example"></a>예제

다음 샘플에서는 C3282 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```
// C3282.cpp
// compile with: /clr /c
generic <typename T> int x;   // C3282

ref struct GC0 {
   generic <typename T> int x;   // C3282
};

// OK
generic <typename T>
ref class M {};
```