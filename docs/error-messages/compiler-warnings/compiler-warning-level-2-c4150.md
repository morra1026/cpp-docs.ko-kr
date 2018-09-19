---
title: 컴파일러 경고 (수준 2) C4150 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4150
dev_langs:
- C++
helpviewer_keywords:
- C4150
ms.assetid: ff1760ec-0d9f-4d45-b797-94261624becf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d317384d3708679d485ae0a77c6ee9b6622b9c83
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46050426"
---
# <a name="compiler-warning-level-2-c4150"></a>컴파일러 경고 (수준 2) C4150

불완전 한 형식 'type';에 대 한 포인터 삭제 소멸자가 호출 되지 않은

합니다 **삭제** 컴파일러가 소멸자를 찾을 수 없습니다 있도록 선언 되었지만 정의 되지 않은 형식을 삭제 하려면 연산자를 호출 합니다.

다음 샘플에서는 C4150 오류가 생성 됩니다.

```
// C4150.cpp
// compile with: /W2
class  IncClass;

void NoDestruct( IncClass* pIncClass )
{
   delete pIncClass;
} // C4150, define class to resolve

int main()
{
}
```