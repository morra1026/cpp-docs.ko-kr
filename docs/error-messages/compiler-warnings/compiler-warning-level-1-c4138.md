---
title: 컴파일러 경고 (수준 1) C4138 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4138
dev_langs:
- C++
helpviewer_keywords:
- C4138
ms.assetid: 65ebf929-bba0-4237-923b-c1b66adfe17d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0d2e637c73482b1a59034d6a269ea2240445bdef
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46046916"
---
# <a name="compiler-warning-level-1-c4138"></a>컴파일러 경고(수준 1) C4138

'*/'가 주석 외부에 있습니다.

닫는 주석 구분 기호 앞에 여는 주석 구분 기호가 없습니다. 컴파일러는 별표 사이 공백이 있다고 가정 (<strong>\*</strong>)와 슬래시 (/).

## <a name="example"></a>예제

```
// C4138a.cpp
// compile with: /W1
int */*comment*/ptr;   // C4138 Ambiguous first delimiter causes warning
int main()
{
}
```

이 경고는 주석을 중첩하려는 경우에 발생할 수 있습니다.

주석을 포함하는 코드 섹션을 주석으로 처리하고 **#if/#endif** 블록에 코드를 포함한 다음 제어하는 식을 0으로 설정하면 이 경고를 해결할 수 있습니다.

```
// C4138b.cpp
// compile with: /W1
#if 0
int my_variable;   /* Declaration currently not needed */
#endif
int main()
{
}
```