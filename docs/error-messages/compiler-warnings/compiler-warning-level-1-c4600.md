---
title: 컴파일러 경고 (수준 1) C4600 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4600
dev_langs:
- C++
helpviewer_keywords:
- C4600
ms.assetid: f023a2a1-7fc4-463f-a434-dc93fcd3f4e9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 27b020fdd87e35633b6a6da74d8c51c63fc1604e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46079364"
---
# <a name="compiler-warning-level-1-c4600"></a>컴파일러 경고(수준 1) C4600

\#pragma '매크로 name': 올바른 비어 있지 않은 문자열이 필요 합니다.

푸시 또는 매크로 이름을 사용 하 여 팝 하는 경우 빈 문자열을 지정할 수 없습니다는 [pop_macro](../../preprocessor/pop-macro.md) 하거나 [push_macro](../../preprocessor/push-macro.md)합니다.

다음 샘플에서는 C4600 오류가 생성 됩니다.

```
// C4600.cpp
// compile with: /W1
int main()
{
   #pragma push_macro("")   // C4600 passing an empty string
}
```