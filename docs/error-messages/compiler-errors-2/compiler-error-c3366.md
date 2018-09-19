---
title: 컴파일러 오류 C3366 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3366
dev_langs:
- C++
helpviewer_keywords:
- C3366
ms.assetid: efc55bcf-c16d-43c1-a36f-87a6165fa2a8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b3638ba2415839c044d9a82d82d0abe8bc2c98e2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026506"
---
# <a name="compiler-error-c3366"></a>컴파일러 오류 C3366

'variable': 관리 되는 정적 데이터 멤버 또는 WinRTtypes 클래스 정의 내에서 정의 해야 합니다

WinRT 또는 .NET 클래스 또는 인터페이스의 정적 멤버를 해당 클래스 또는 인터페이스의 정의 외부에서 참조하려고 했습니다.

컴파일러는 한 번 통과한 후 메타데이터를 내보내기 위해 클래스의 전체 정의를 알아야 하며 클래스 내에서 정적 데이터 멤버가 초기화되어야 합니다.

예를 들어 다음 예제에서는 C3366 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```
// C3366.cpp
// compile with: /clr /c
ref class X {
   public:
   static int i;   // initialize i here to avoid C3366
};

int X::i = 5;      // C3366
```
