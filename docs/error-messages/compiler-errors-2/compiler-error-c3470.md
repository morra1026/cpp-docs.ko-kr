---
title: 컴파일러 오류 C3470 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3470
dev_langs:
- C++
helpviewer_keywords:
- C3470
ms.assetid: 170c7a9d-214d-41b1-8f15-d4a4fc38aaa5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0e9d09e421b7a38a99f70f0ee8fa158127787cae
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46107548"
---
# <a name="compiler-error-c3470"></a>컴파일러 오류 C3470

'type': 클래스에 인덱서(인덱싱된 기본 속성)와 operator[]가 동시에 포함될 수 없습니다.

하나의 형식으로 기본 인덱서와 연산자[]를 모두 정의할 수 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3470을 생성합니다.

```
// C3470.cpp
// compile with: /clr
using namespace System;

ref class R {
public:
   property int default[int] {
      int get(int i) {
         return i+1;
      }
   }

   int operator[](String^ s) { return Convert::ToInt32(s); }   // C3470
};

int main() {
   R ^ r = gcnew R;
   // return r[9] + r["32"] - 42;
}
```