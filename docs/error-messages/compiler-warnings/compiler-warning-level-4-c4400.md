---
title: 컴파일러 경고 (수준 4) C4400 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4400
dev_langs:
- C++
helpviewer_keywords:
- C4400
ms.assetid: f135fe98-4f92-4e07-9d71-2621b36ee755
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cd22db0313d2d0ea6494908259e7d098336f6dbd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016197"
---
# <a name="compiler-warning-level-4-c4400"></a>컴파일러 경고(수준 4) C4400

'type':이 형식에서 const/volatile 한정자는 지원 되지 않습니다

합니다 [const](../../cpp/const-cpp.md)하 고 [volatile](../../cpp/volatile-cpp.md)한정자가 공용 언어 런타임 형식의 변수를 사용 하 여 작동 하지 것입니다.

## <a name="example"></a>예제

다음 샘플 C4400를 생성합니다.

```
// C4400.cpp
// compile with: /clr /W4
// C4401 expected
using namespace System;
#pragma warning (disable : 4101)
int main() {
   const String^ str;   // C4400
   volatile String^ str2;   // C4400
}
```