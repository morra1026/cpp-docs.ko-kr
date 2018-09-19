---
title: 컴파일러 오류 C2645 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2645
dev_langs:
- C++
helpviewer_keywords:
- C2645
ms.assetid: 6609c2fa-c3b2-4a6b-8e8d-58fb52f67175
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2ada345b79c061c71bc716bf7baf96116444bcc7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46076829"
---
# <a name="compiler-error-c2645"></a>컴파일러 오류 C2645

멤버에 대 한 포인터에 대 한 정규화 된 이름이 없는 (찾을 수 ':: *')

멤버에 대 한 포인터의 선언에서 클래스를 지정 하지 않습니다.

다음 샘플에서는 C2645 오류가 생성 됩니다.

```
// C2645.cpp
class A {};
int main() {
   int B::* bp;   // C2645 B not defined
   int A::* ap;   // OK
}
```