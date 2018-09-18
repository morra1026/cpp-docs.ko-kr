---
title: 컴파일러 오류 C2140 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2140
dev_langs:
- C++
helpviewer_keywords:
- C2140
ms.assetid: d44a0500-002c-4632-9e5e-c71c3a473ec4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3fc0bd6fd0a43b8071a9872c9c1a598b57e090c3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46065402"
---
# <a name="compiler-error-c2140"></a>컴파일러 오류 C2140

'type': 제네릭 형식 매개 변수에 종속 된 형식은 컴파일러 내장 형식 특성 '특성 (trait)'에 대 한 인수로 사용할 수 없습니다

잘못 된 형식 지정자는 형식 특성에 전달 되었습니다.

자세한 내용은 [형식 특성에 대 한 컴파일러 지원](../../windows/compiler-support-for-type-traits-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C2140를 생성합니다.

```
// C2140.cpp
// compile with: /clr /c
template <class T>

struct is_polymorphic {
   static const bool value = __is_polymorphic(T);
};

class x {};

generic <class T>
ref class C {
   void f() {
      System::Console::WriteLine(__is_polymorphic(T));   // C2140
      System::Console::WriteLine(is_polymorphic<T>::value);   // C2140

      System::Console::WriteLine(__is_polymorphic(x));   // OK
      System::Console::WriteLine(is_polymorphic<x>::value);   // OK
   }
};
```