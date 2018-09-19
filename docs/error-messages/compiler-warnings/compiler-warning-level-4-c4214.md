---
title: 컴파일러 경고 (수준 4) C4214 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4214
dev_langs:
- C++
helpviewer_keywords:
- C4214
ms.assetid: 9b8db279-1f12-4a6b-a923-2db22acd1947
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 879c959bfe851b56dbc60b4eeb714db8d7f9dfaf
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46027429"
---
# <a name="compiler-warning-level-4-c4214"></a>컴파일러 경고(수준 4) C4214

비표준 확장이 사용 됨: 비트 필드 형식이 int

기본 Microsoft 확장명 (/Ze)를 사용 하 여 모든 정수 형식의 비트 필드 구조체 멤버 수 있습니다.

## <a name="example"></a>예제

```
// C4214.c
// compile with: /W4
struct bitfields
{
   unsigned short j:4;  // C4214
};

int main()
{
}
```

이러한 비트 필드를 ANSI 호환성 올바르지 않습니다 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).