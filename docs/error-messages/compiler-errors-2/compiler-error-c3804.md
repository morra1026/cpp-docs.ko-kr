---
title: 컴파일러 오류 C3804 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3804
dev_langs:
- C++
helpviewer_keywords:
- C3804
ms.assetid: 7c4cda28-ec96-4d04-937b-36dbd9944722
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6ef798ec8697ee9a856162b9aa63ccbf23db15f7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46113203"
---
# <a name="compiler-error-c3804"></a>컴파일러 오류 C3804

'property_accessor': 접근자 메서드는 속성은 수 모두 static 이거나 모두 static이 아니고

접근자 함수를 정적 수 특수 속성을 정의 하는 경우 또는 인스턴스를 하나만 있습니다.

자세한 내용은 [property](../../windows/property-cpp-component-extensions.md) 를 참조하세요.

## <a name="example"></a>예제

다음 샘플 C3804를 생성합니다.

```
// C3804.cpp
// compile with: /c /clr
ref struct A {

   property int i {
      static int get() {}
      void set(int i) {}
   }   // C3804 error

   // OK
   property int j {
      int get() { return 0; }
      void set(int i) {}
   }

   property int k {
      static int get() { return 0; }
      static void set(int i) {}
   }
};
```