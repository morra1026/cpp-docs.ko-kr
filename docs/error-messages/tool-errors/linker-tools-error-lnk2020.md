---
title: 링커 도구 오류 LNK2020 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK2020
dev_langs:
- C++
helpviewer_keywords:
- LNK2020
ms.assetid: 4dd017d0-5e83-471b-ac8a-538ac1ed6870
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 90088d311bac7ee4ce59797d5dcbe148a24963f6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46034969"
---
# <a name="linker-tools-error-lnk2020"></a>링커 도구 오류 LNK2020

확인 되지 않은 ' token '토큰

유사 하지만 정의 되지 않은 외부 오류가 된다는 점이 메타 데이터를 통해 참조 됩니다. 메타 데이터의 모든 함수 및 데이터를 정의 합니다.

해결 방법:

- 누락 된 함수 또는 데이터를 정의 합니다. 또는

- 개체 파일 또는 누락 된 함수 또는 데이터는 이미 정의 된 라이브러리를 포함 합니다.

## <a name="example"></a>예제

다음 샘플 LNK2020를 생성합니다.

```
// LNK2020.cpp
// compile with: /clr /LD
ref struct A {
   A(int x);   // LNK2020
   static int f();   // LNK2020
};

// OK
ref struct B {
   B(int x) {}
   static int f() { return 0; }
};
```

## <a name="example"></a>예제

LNK2020는 관리 되는 템플릿 형식의 변수를 만들지만 형식을 인스턴스화하지 않습니다 하는 경우에 발생 합니다.

다음 샘플 LNK2020를 생성합니다.

```
// LNK2020_b.cpp
// compile with: /clr

template <typename T>
ref struct Base {
   virtual void f1() {};
};

template <typename T>
ref struct Base2 {
   virtual void f1() {};
};

int main() {
   Base<int>^ p;   // LNK2020
   Base2<int>^ p2 = gcnew Base2<int>();   // OK
};
```