---
title: 컴파일러 오류 C2139 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2139
dev_langs:
- C++
helpviewer_keywords:
- C2139
ms.assetid: 31e047c0-5bf9-46c2-b6de-b627ea6a5768
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7b8da6a8bb4ca7630a3deff3b1ec79ca512ae2e0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46090102"
---
# <a name="compiler-error-c2139"></a>컴파일러 오류 C2139

'type': 컴파일러 내장 형식 특성 '특성 (trait)'에 대 한 인수로 정의 되지 않은 클래스는 사용할 수 없습니다

형식 특성에 잘못 된 인수가 전달 되었습니다.

자세한 내용은 [형식 특성에 대 한 컴파일러 지원](../../windows/compiler-support-for-type-traits-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C2139를 생성합니다.

```
// C2139.cpp
// compile with: /EHsc
#include <iostream>
using namespace std;

template <class T>
struct is_polymorphic {
   static const bool value = __is_polymorphic(T);
};

class C;
class D {};

class E {
public:
   virtual void Test() {}
};

int main() {
   cout << is_polymorphic<C>::value << endl;   // C2139
   cout << is_polymorphic<D>::value << endl;   // OK
   cout << is_polymorphic<E>::value << endl;   // OK
}
```