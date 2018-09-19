---
title: 컴파일러 오류 C2750 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2750
dev_langs:
- C++
helpviewer_keywords:
- C2750
ms.assetid: 30450034-feb5-448c-9655-b8c5f3639695
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e3f40894c4879c9b3598429c02bb0811db658bb0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46069516"
---
# <a name="compiler-error-c2750"></a>컴파일러 오류 C2750

'type': 참조 형식에 'new' 사용할 수 없습니다 'gcnew'를 대신 사용

그러면 인스턴스가 가비지 수집 힙에 배치 될 CLR 형식의 인스턴스를 만드는 사용 해야 합니다 [gcnew](../../windows/ref-new-gcnew-cpp-component-extensions.md)합니다.

다음 샘플에서는 C2750를 생성합니다.

```
// C2750.cpp
// compile with: /clr
ref struct Y1 {};

int main() {
   Y1 ^ x = new Y1;   // C2750

   // try the following line instead
   Y1 ^ x2 = gcnew Y1;
}
```