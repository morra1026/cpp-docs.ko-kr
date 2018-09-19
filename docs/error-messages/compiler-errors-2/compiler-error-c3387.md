---
title: 컴파일러 오류 C3387 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3387
dev_langs:
- C++
helpviewer_keywords:
- C3387
ms.assetid: c54d9925-ed14-4976-b8db-e8d4dc84e536
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0dafe972db1b3210e9243e34cc02e7a0366bdd65
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46030757"
---
# <a name="compiler-error-c3387"></a>컴파일러 오류 C3387

'member': __declspec (dllexport) /\__declspec(dllimport) 멤버 관리 되는 또는 WinRT 형식에 적용할 수 없습니다

`dllimport` 하 고 [dllexport](../../cpp/dllexport-dllimport.md) `__declspec` 한정자 관리 되는 멤버 또는 Windows 런타임 형식에서 유효 하지 않습니다.

다음 샘플에서는 C3387 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```
// C3387a.cpp
// compile with: /clr /c
ref class X2 {
   void __declspec(dllexport) mf() {   // C3387
   // try the following line instead
   // void mf() {
   }
};
```