---
title: 컴파일러 오류 C2593 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2593
dev_langs:
- C++
helpviewer_keywords:
- C2593
ms.assetid: 4a0fe9bb-2163-447d-91f6-1890ed8250f6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1a3b0d1a8574aa5c05bbca023a1209cf1801f57e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46042730"
---
# <a name="compiler-error-c2593"></a>컴파일러 오류 C2593

'연산자 identifier' 모호합니다.

둘 이상의 가능한 연산자를 오버 로드 된 연산자에 대해 정의 됩니다.

하나 이상의 실제 매개 변수에서 명시적 캐스트를 사용 하는 경우이 오류를 해결할 수 있습니다.

다음 샘플에서는 C2593을 생성합니다.

```
// C2593.cpp
struct A {};
struct B : A {};
struct X {};
struct D : B, X {};
void operator+( X, X );
void operator+( A, B );
D d;

int main() {
   d +  d;         // C2593, D has an A, B, and X
   (X)d + (X)d;    // OK, uses operator+( X, X )
}
```

이 오류를 사용 하 여 부동 소수점 변수를 직렬화 하 여 발생할 수 있습니다는 `CArchive` 개체입니다. 컴파일러 하 게 식별 하는 `<<` 모호 하다는 연산자입니다. 기본 c + + 형식에 `CArchive` serialize 할 수는 고정 크기 형식 `BYTE`를 `WORD`, `DWORD`, 및 `LONG`합니다. 모든 정수 형식 serialization에 대 한 이러한 형식 중 하나로 캐스팅 되어야 합니다. 부동 소수점 형식을 사용 하 여 보관 해야 합니다 `CArchive::Write()` 멤버 함수입니다.

다음 예제에서는 부동 소수점 변수에 보관 하는 방법을 보여 줍니다 (`f`)에서 보관 `ar`:

```
ar.Write(&f, sizeof( float ));
```