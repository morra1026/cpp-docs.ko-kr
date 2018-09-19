---
title: 컴파일러 경고 (수준 4) C4220 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4220
dev_langs:
- C++
helpviewer_keywords:
- C4220
ms.assetid: aba18868-825f-4763-9af6-3296406a80e4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 70c6b104c924a09570d4bd77191f1df715726370
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118780"
---
# <a name="compiler-warning-level-4-c4220"></a>컴파일러 경고(수준 4) C4220

varargs는 나머지 매개 변수와 일치

기본 Microsoft 확장 (/Ze)에서는 함수에 대 한 포인터와 유사 하지만 변수, 인수를 사용 하 여 함수에 대 한 포인터를 일치합니다.

## <a name="example"></a>예제

```
// C4220.c
// compile with: /W4

int ( *pFunc1) ( int a, ... );
int ( *pFunc2) ( int a, int b);

int main()
{
   if ( pFunc1 != pFunc2 ) {};  // C4220
}
```

이러한 포인터는 ANSI 호환성 일치 하지 않습니다 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).