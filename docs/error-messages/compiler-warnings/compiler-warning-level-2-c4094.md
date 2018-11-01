---
title: 컴파일러 경고 (수준 2) C4094
ms.date: 11/04/2016
f1_keywords:
- C4094
helpviewer_keywords:
- C4094
ms.assetid: e68929fb-3a1c-4be7-920b-d5f79f534f99
ms.openlocfilehash: 73805afc897d14c6d2cc87490dfa0769a8de5193
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50488402"
---
# <a name="compiler-warning-level-2-c4094"></a>컴파일러 경고 (수준 2) C4094

태그가 지정 되지 않은 ' token' 기호가 없는 선언

컴파일러는 태그가 지정 되지 않은 구조체, 공용 구조체 또는 클래스를 사용 하 여 빈 선언을 발견 했습니다. 선언이 무시 됩니다.

## <a name="example"></a>예제

```
// C4094.cpp
// compile with: /W2
struct
{
};   // C4094

int main()
{
}
```

ANSI 호환성 오류를 생성 하는이 조건 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).