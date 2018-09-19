---
title: 컴파일러 경고 (수준 1) C4091 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4091
dev_langs:
- C++
helpviewer_keywords:
- C4091
ms.assetid: 3a404967-ab42-49b0-b324-fd7ba1859d78
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7b8fd377ed8b1f6425f0a1c13a83531fca1b797f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46114100"
---
# <a name="compiler-warning-level-1-c4091"></a>컴파일러 경고 (수준 1) C4091

'keyword': 변수가 없으면 선언 되 면 왼쪽 'type'은 무시 됩니다

컴파일러는 사용자를 선언 하는 변수를 위한 것 하지만 컴파일러에서 변수를 선언할 수 없습니다 경우를 발견 했습니다.

## <a name="example"></a>예제

`__declspec` 특성을 사용자 정의 형식 선언의 시작 부분에서 해당 형식의 변수에 적용 됩니다. C4091 선언 된 변수가 없음을 나타냅니다. 다음 샘플 C4091를 생성합니다.

```
// C4091.cpp
// compile with: /W1 /c
__declspec(dllimport) class X {}; // C4091

// __declspec attribute applies to varX
__declspec(dllimport) class X2 {} varX;

// __declspec attribute after the class or struct keyword
// applies to user defined type
class __declspec(dllimport) X3 {};
```

## <a name="example"></a>예제

식별자 형식 정의 인 경우 변수 이름을 수도 없습니다. 다음 샘플 C4091를 생성합니다.

```
// C4091_b.cpp
// compile with: /c /W1 /WX
#define LIST 4
typedef struct _LIST {} LIST;   // C4091
```