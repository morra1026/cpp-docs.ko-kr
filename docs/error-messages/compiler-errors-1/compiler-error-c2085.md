---
title: 컴파일러 오류 C2085 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2085
dev_langs:
- C++
helpviewer_keywords:
- C2085
ms.assetid: 0a86785c-8e6f-481b-8c7b-412220c1950d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d88968e49e38a13782dde2d905a614ad4d177e81
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46082380"
---
# <a name="compiler-error-c2085"></a>컴파일러 오류 C2085

'identifier': 정식 매개 변수 목록에 없는

식별자는 정식 매개 변수 목록이 아니라 함수 정의에서 선언 되었습니다. (ANSI C에만 해당)

다음 샘플에서는 C2085 오류가 생성 됩니다.

```
// C2085.c
void func1( void )
int main( void ) {}   // C2085
```

해결 방법:

```
// C2085b.c
void func1( void );
int main( void ) {}
```

세미콜론 누락 된 `func1()` 프로토타입이 아니라 함수 정의 따라서 같습니다 `main` 내에 정의 되어 `func1()`를 식별자에 대 한 오류 c2085 `main`합니다.