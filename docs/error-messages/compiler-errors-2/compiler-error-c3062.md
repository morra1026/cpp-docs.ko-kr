---
title: 컴파일러 오류 C3062
ms.date: 11/04/2016
f1_keywords:
- C3062
helpviewer_keywords:
- C3062
ms.assetid: 78632e6d-255f-42c3-b124-31a9194ff86d
ms.openlocfilehash: ac45847c94e7d2dc731eba71b0a38105eb915e53
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50590413"
---
# <a name="compiler-error-c3062"></a>컴파일러 오류 C3062

'enum': 기본 형식 'type' 이므로 열거자 값이 필요

열거형에 대 한 기본 형식을 지정할 수 있습니다. 그러나 일부 형식에 각 열거자에 값을 할당 해야 합니다.

열거형에 대 한 자세한 내용은 참조 하세요. [enum 클래스](../../windows/enum-class-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3062 오류가 생성 됩니다.

```
// C3062.cpp
// compile with: /clr

enum class MyEnum : bool { a };   // C3062
enum class MyEnum2 : bool { a = true};   // OK
```