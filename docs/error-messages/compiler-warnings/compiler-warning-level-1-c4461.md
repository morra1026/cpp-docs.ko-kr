---
title: 컴파일러 경고 (수준 1) C4461 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4461
dev_langs:
- C++
helpviewer_keywords:
- C4461
ms.assetid: 104ffecc-3dd4-4cb1-89a8-81154fbe46d9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 86c12208c6992b97f30bc36ea821ba26148ff751
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46081402"
---
# <a name="compiler-warning-level-1-c4461"></a>컴파일러 경고(수준 1) C4461

'type':이 클래스에 'finalizer'는 종료 자가 있지만 'dtor' 소멸자가 없습니다

형식에 종료자의 존재를 삭제 하는 리소스를 의미 합니다. 해당 형식의 소멸자에서 종료자는 명시적으로 호출 하지 않는 한 개체 범위를 벗어난 후 종료자를 실행 하는 경우 공용 언어 런타임에서 결정 합니다.

형식에서 소멸자를 정의 하 고 명시적으로 소멸자에서 종료자를 호출 하는 경우 종료자를 명확 하 게 실행할 수 있습니다.

자세한 내용은 [소멸자 및 종료자](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers)합니다.

## <a name="example"></a>예제

다음 샘플 C4461를 생성합니다.

```
// C4461.cpp
// compile with: /W1 /clr /c
ref class A {
protected:
   !A() {}   // C4461
};

// OK
ref struct B {
   ~B() {
      B::!B();
   }

   !B() {}
};
```