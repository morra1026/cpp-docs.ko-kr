---
title: 컴파일러 오류 C3390 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3390
dev_langs:
- C++
helpviewer_keywords:
- C3390
ms.assetid: 84800a87-c8e6-45aa-82ae-02f816dc8d97
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f7f1a19d86e133d01a17703f7ef4b3a79d5eb601
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46111994"
---
# <a name="compiler-error-c3390"></a>컴파일러 오류 C3390

'type_arg': 제네릭 'generic_type'의 제네릭 매개 변수 'param'에 대한 형식 인수가 잘못되었습니다. 참조 형식이어야 합니다.

제네릭 형식이 잘못 인스턴스화되었습니다.  형식 정의를 확인하세요.  자세한 내용은 [제네릭](../../windows/generics-cpp-component-extensions.md)을 참조하세요.

## <a name="example"></a>예제

C +의 제네릭 형식을 제작 하는 경우 지원 되지 않는 특정 제약 조건이 있는 제네릭 형식을 포함 하는 구성 요소를 만드는 첫 번째 예제에서는 C# + CLR. 자세한 내용은 [형식 매개 변수에 대한 제약 조건](/dotnet/csharp/programming-guide/generics/constraints-on-type-parameters)을 참조하세요.

```cs
// C3390.cs
// Compile by using: csc /target:library C3390.cs
// a C# program
public class GR<C, V, N>
where C : class
where V : struct
where N : new() {}
```

C3390.dll 구성 요소를 사용할 수 있는 경우 다음 샘플에서는 C3390을 생성 합니다.

```cpp
// C3390_b.cpp
// Compile by using: cl /clr C3390_b.cpp
#using <C3390.dll>
ref class R { R(int) {} };
value class V {};
ref struct N { N() {} };

int main () {
   GR<V, V, N^>^ gr2;   // C3390 first type must be a ref type
   GR<R^, V, N^>^ gr2b; // OK
}
```