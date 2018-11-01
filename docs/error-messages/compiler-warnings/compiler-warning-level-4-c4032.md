---
title: 컴파일러 경고 (수준 4) C4032
ms.date: 11/04/2016
f1_keywords:
- C4032
helpviewer_keywords:
- C4032
ms.assetid: 70dd0c85-0239-43f9-bb06-507f6a57d206
ms.openlocfilehash: fa1602d63ed9822725fea8e1b842929f221d3926
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50657303"
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