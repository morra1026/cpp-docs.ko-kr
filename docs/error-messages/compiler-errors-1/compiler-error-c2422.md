---
title: 컴파일러 오류 C2422 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2422
dev_langs:
- C++
helpviewer_keywords:
- C2422
ms.assetid: ef0ec302-4028-4778-b134-0b8cea4bcad9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 17421f2d4a7823c0e2fbb34a54a7c562223c798c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46047033"
---
# <a name="compiler-error-c2422"></a>컴파일러 오류 C2422

'피연산자'에 잘못 된 세그먼트 재정의가 있습니다.

인라인 어셈블리 코드를 잘못 사용 했습니다 없습니다 세그먼트 재정의 연산자 (콜론) 피연산자에 사용할 수 있습니다.  이 오류가 발생하는 원인은 다음과 같습니다.

- 연산자 앞에 오는 레지스터 세그먼트 레지스터가 아닙니다.

- 연산자 앞에 오는 레지스터 피연산자의 세그먼트 레지스터가 아닙니다.

- 세그먼트 재정의 연산자를 간접 참조 연산자 (대괄호) 내에 나타납니다.

- 다음에 나오는 세그먼트 재정의 연산자는 식 즉 치 피연산자는 또는 메모리 피연산자 아닙니다.

다음 샘플에서는 C2422 오류가 생성 됩니다.

```
// C2422.cpp
// processor: x86
int main() {
   _asm {
      mov AX, [BX:ES]   // C2422
      mov AX, ES   // OK
   }
}
```