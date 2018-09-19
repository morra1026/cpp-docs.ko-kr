---
title: 컴파일러 오류 C2752 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2752
dev_langs:
- C++
helpviewer_keywords:
- C2752
ms.assetid: ae42b3ec-84a9-4e9d-8d59-3d208132d0b2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ea33ef80847a8699115a92e316fec156c3c51607
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46081652"
---
# <a name="compiler-error-c2752"></a>컴파일러 오류 C2752

'template': 둘 이상의 부분 특수화는 템플릿 인수 목록과 일치 합니다.

인스턴스화가 모호 합니다.

다음 샘플에서는 C2752를 생성합니다.

```
// C2752.cpp
template<class T, class U>
struct A {};

template<class T, class U>
struct A<T*, U> {};

template<class T, class U>
struct A<T,U*> {};

// try the following line instead
// template<class T, class U> struct A<T*,U*> {};

int main() {
   A<char*,int*> a;   // C2752 an instantiation

   // OK
   A<char*,int> a1;
   A<char,int*> a2;
   A<char,int> a3;
}
```