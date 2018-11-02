---
title: 컴파일러 경고(수준 1) C4518
ms.date: 11/04/2016
f1_keywords:
- C4518
helpviewer_keywords:
- C4518
ms.assetid: 4ad21004-f076-43fd-99f4-4bf1f9be4c0b
ms.openlocfilehash: 85e0d87094fc355bf63d79bf2eb5b1d06f233542
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50466809"
---
# <a name="compiler-warning-level-1-c4518"></a>컴파일러 경고(수준 1) C4518

'specifier': 저장소 클래스 또는 형식 지정 자가 예기치 않은. 무시

다음 샘플에서는 C4518 오류가 생성 됩니다.

```
// C4518.cpp
// compile with: /c /W1
_declspec(dllexport) extern "C" void MyFunction();   // C4518

extern "C" void MyFunction();   // OK
```