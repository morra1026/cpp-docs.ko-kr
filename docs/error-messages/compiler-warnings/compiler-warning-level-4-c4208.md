---
title: 컴파일러 경고 (수준 4) C4208 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4208
dev_langs:
- C++
helpviewer_keywords:
- C4208
ms.assetid: 5cb0a36e-3fb5-422f-a5f9-e40b70776c27
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8ee87ad1d43b20c4d0a72b877b05b1ba4c084a1a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064624"
---
# <a name="compiler-warning-level-4-c4208"></a>컴파일러 경고(수준 4) C4208

비표준 확장이 사용 됨: delete [exp]-exp가 계산 되지만 무시

Microsoft 확장 (/Ze)을 사용 하 여는 괄호 안의 값을 사용 하 여 배열을 삭제할 수 있습니다 합니다 [delete 연산자](../../cpp/delete-operator-cpp.md)합니다. 값은 무시 됩니다.

```
// C4208.cpp
// compile with: /W4
int main()
{
   int * MyArray = new int[18];
   delete [18] MyArray;      // C4208
   MyArray = new int[18];
   delete [] MyArray;        // ok
}
```

이러한 값이 잘못 ANSI 호환성 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).