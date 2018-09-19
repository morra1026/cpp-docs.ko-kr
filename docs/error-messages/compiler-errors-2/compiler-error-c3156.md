---
title: 컴파일러 오류 C3156 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3156
dev_langs:
- C++
helpviewer_keywords:
- C3156
ms.assetid: 1876da78-b94e-4af7-9795-28f72b209b3e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cfb52ad730df486ee804bcf958505512fadc0150
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46116706"
---
# <a name="compiler-error-c3156"></a>컴파일러 오류 C3156

'class': 관리되는 또는 WinRT 형식의 지역 정의를 사용할 수 없습니다.

함수에 관리되는 또는 WinRT 클래스, 구조체 또는 인터페이스의 정의 또는 선언을 포함할 수 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3156를 생성합니다.

```
// C3156.cpp
// compile with: /clr /c
void f() {
   ref class X {};   // C3156
   ref class Y;   // C3156
}
```
