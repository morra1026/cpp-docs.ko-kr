---
title: 컴파일러 오류 C3384
ms.date: 11/04/2016
f1_keywords:
- C3384
helpviewer_keywords:
- C3384
ms.assetid: c9f92c6a-62a9-4333-b2b1-bc55c7f288b6
ms.openlocfilehash: 0c9804666bfd73f98541f95434b9cebf5185d2ed
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50566818"
---
# <a name="compiler-error-c3384"></a>컴파일러 오류 C3384

'type_parameter': 값 제약 조건과 ref 제약 조건은 함께 사용할 수 없습니다.

제네릭 형식을 `value class` 및 `ref class`둘 다로 제한할 수 없습니다.

참조 [제네릭 형식 매개 변수에 대 한 제약 조건 (C + + /cli CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md) 자세한 내용은 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3384를 생성합니다.

```
// C3384.cpp
// compile with: /c /clr
generic <typename T>
where T : ref class
where T : value class   // C3384
ref class List {};
```