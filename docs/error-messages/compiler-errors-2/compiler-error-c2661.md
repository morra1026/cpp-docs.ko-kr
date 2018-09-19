---
title: 컴파일러 오류 C2661 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2661
dev_langs:
- C++
helpviewer_keywords:
- C2661
ms.assetid: 60021467-71cd-451b-9877-23840c69309f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a8443e21db273aa7def879bd82ab823afb8a508a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074398"
---
# <a name="compiler-error-c2661"></a>컴파일러 오류 C2661

'function': 오버 로드 된 함수가 없는 숫자 매개 변수를 사용 합니다.

가능한 원인:

1. 함수 호출에서 실제 매개 변수가 잘못 되었습니다.

1. 함수 선언이 없습니다.

다음 샘플에서는 C2661 오류가 생성 됩니다.

```
// C2661.cpp
void func( int ){}
void func( int, int ){}
int main() {
   func( );   // C2661 func( void ) was not declared
   func( 1 );   // OK func( int ) was declared
}
```