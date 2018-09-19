---
title: 컴파일러 경고 (수준 1) C4927 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4927
dev_langs:
- C++
helpviewer_keywords:
- C4927
ms.assetid: 7009e740-a2ef-4130-96ba-482e092f717a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2144a1315870f0202962652fd0056e42e5562665
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46031192"
---
# <a name="compiler-warning-level-1-c4927"></a>컴파일러 경고(수준 1) C4927

변환이 잘못 되었습니다. 둘 이상의 사용자 정의 변환이 암시적으로 적용 된

둘 이상의 사용자 정의 변환이 암시적으로 단일 값-에 적용 되었습니다. 컴파일러 변환 하는 명시적 변환을 찾을 수 없습니다 하지만 해당 하는 변환의 찾을.

다음 샘플에서는 C4927 오류가 생성 됩니다.

```
// C4927.cpp
// compile with: /W1
struct B
{
   operator int ()
   {
      return 0;
   }
};

struct A
{
   A(int i)
   {
   }

   /*
   // uncomment this constructor to resolve
   A(B b)
   {
   }
   */
};

A f1( B& b)
{
   return A(b);
}

B& f2( B& b)
{
   return b;
}

A f()
{
   B b;
   return A(b);   // ok
   return f1(b);  // ok
   return b;      // C4927
   return B(b);   // C4927
   return f2(b);  // C4927
}

int main()
{
   B b;
   A a = b;
   A a2(b);
}
```