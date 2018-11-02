---
title: 컴파일러 오류 C3393
ms.date: 11/04/2016
f1_keywords:
- C3393
helpviewer_keywords:
- C3393
ms.assetid: d57f7c69-0a02-4fe3-9e45-bc62644fd77c
ms.openlocfilehash: d2822d5a36b2091881d354131b2a28d386f787c0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50520469"
---
# <a name="compiler-error-c3393"></a>컴파일러 오류 C3393

제약 조건 절의 구문 오류: 'identifier'가 형식이 아닙니다.

제약 조건에 전달된 식별자가 형식이어야 하는 데 형식이 아닙니다.  자세한 내용은 [제네릭 형식 매개 변수에 대 한 제약 조건 (C + + CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3393을 생성합니다.

```
// C3393.cpp
// compile with: /clr /c
void MyInterface() {}
interface class MyInterface2 {};

generic<typename T>
where T : MyInterface   // C3393
// try the following line instead
// where T : MyInterface2
ref class R {};
```