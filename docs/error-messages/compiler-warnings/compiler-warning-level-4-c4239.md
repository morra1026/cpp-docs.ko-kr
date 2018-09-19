---
title: 컴파일러 경고 (수준 4) C4239 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4239
dev_langs:
- C++
helpviewer_keywords:
- C4239
ms.assetid: a23dc16a-649e-4870-9a24-275de1584fcd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 89a68de05ff999e72fc02a75d5958a7e2589f8ed
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032844"
---
# <a name="compiler-warning-level-4-c4239"></a>컴파일러 경고(수준 4) C4239

비표준 확장이 사용 됨: 'token': 'type'에서 'type'로 변환

C + + 표준에서는이 형식으로 변환할 수 없습니다 있지만 허용 된 확장으로 여기 있습니다. 이 경고 뒤에 항상 하나 이상의 줄을 위반 하는 언어 규칙을 설명 하는 설명.

## <a name="example"></a>예제

다음 샘플 C4239를 생성합니다.

```
// C4239.cpp
// compile with: /W4 /c
struct C {
   C() {}
};

void func(void) {
   C & rC = C();   // C4239
   const C & rC2 = C();   // OK
   rC2;
}
```

## <a name="example"></a>예제

정수 계열 형식에서 열거형 형식 변환할 엄격 하 게 허용 되지 않습니다.

다음 샘플 C4239를 생성합니다.

```
// C4239b.cpp
// compile with: /W4 /c
enum E { value };
struct S {
   E e : 2;
} s = { 5 };   // C4239
// try the following line instead
// } s = { (E)5 };
```