---
title: 컴파일러 경고 (수준 4) C4032 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4032
dev_langs:
- C++
helpviewer_keywords:
- C4032
ms.assetid: 70dd0c85-0239-43f9-bb06-507f6a57d206
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 608c99c81fac0088a4d1d8bb8a6d3b0b61c7af50
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46086041"
---
# <a name="compiler-warning-level-4-c4032"></a>컴파일러 경고 (수준 4) C4032

형식 매개 변수 'number'의 형식이 다릅니다.

매개 변수 형식을 이전 선언에서 형식 사용 하 여 기본 프로 모션을 통해 호환 되지 않습니다.

이것은 ANSI C에서 오류 ([/Za](../../build/reference/za-ze-disable-language-extensions.md))을 Microsoft 확장 (/Ze)는 경고가 발생 합니다.

## <a name="example"></a>예제

```
// C4032.c
// compile with: /W4
void func();
void func(char);   // C4032, char promotes to int

int main()
{
}
```