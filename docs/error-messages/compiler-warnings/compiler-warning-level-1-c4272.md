---
title: 컴파일러 경고 (수준 1) C4272 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4272
dev_langs:
- C++
helpviewer_keywords:
- C4272
ms.assetid: 0d6c1de4-2eef-42c4-b861-c221f8b495ef
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 00e30646c9fe56132da9cf87ba71cb54ae6a3e8f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052961"
---
# <a name="compiler-warning-level-1-c4272"></a>컴파일러 경고(수준 1) C4272

'function': __declspec (dllimport); 표시 함수를 가져올 때에 네이티브 호출 규칙을 지정 해야 합니다.

사용 하 여 표시 된 함수를 내보내려면 오류가 발생 합니다 [__clrcall](../../cpp/clrcall.md) 표시 된 함수를 가져오려는 경우이 경고가 발생 호출 규칙 및 컴파일러 `__clrcall`합니다.

다음 샘플에서는 C4272 오류가 생성 됩니다.

```
// C4272.cpp
// compile with: /c /W1 /clr
__declspec(dllimport) void __clrcall Test();   // C4272
__declspec(dllimport) void Test2();   // OK
```