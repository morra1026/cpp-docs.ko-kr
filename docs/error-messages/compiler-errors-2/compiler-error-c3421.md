---
title: 컴파일러 오류 C3421 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3421
dev_langs:
- C++
helpviewer_keywords:
- C3421
ms.assetid: b52050c6-17a4-424a-8894-337b0cec7010
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 815fc64e1f2cc80440e188d944827820bd55383b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46114542"
---
# <a name="compiler-error-c3421"></a>컴파일러 오류 C3421

'type': 이 클래스의 종료자는 액세스할 수 없거나 존재하지 않으므로 호출할 수 없습니다.

종료자는 암시적으로 비공개이므로 바깥쪽 형식 외부에서 호출될 수 없습니다.

자세한 내용은 [방법의 소멸자 및 종료자: 클래스 및 구조체 정의 및 사용 (C + + /cli CLI)](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3421을 생성합니다.

```
// C3421.cpp
// compile with: /clr
ref class A {};

ref class B {
   !B() {}

public:
   ~B() {}
};

int main() {
   A a;
   a.!A();   // C3421

   B b;
   b.!B();   // C3421
}
```