---
title: 컴파일러 오류 C2084 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2084
dev_langs:
- C++
helpviewer_keywords:
- C2084
ms.assetid: 990b107f-3721-4851-ae8b-4b69a8c149ed
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 09ce703b6908257e37c2b7ff1b2714f1426f941f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052116"
---
# <a name="compiler-error-c2084"></a>컴파일러 오류 C2084

함수 '*함수*' 이미 본문이 있습니다.

함수가 이미 정의 되었습니다.

Visual Studio 2002 년 이전 Visual c + + 버전

- 추가 정의 사용할 수 없는 있지만 컴파일러에서 동일한 실제 형식으로 확인 하는 여러 템플릿 특수화를 수락 했습니다. 컴파일러는 이제 이러한 여러 정의 검색합니다.

- `__int32` 및 `int` 별도 형식으로 간주 되었습니다. 이제는 컴파일러에서 간주 `__int32` 의 동의어로 `int`합니다. 즉, 둘 다에서 함수는 오버 로드 하는 경우 컴파일러 여러 정의 검색 하는지 `__int32` 및 `int` 및 오류가 발생 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2084 오류가 생성 됩니다.

```cpp
// C2084.cpp
void Func(int);
void Func(int) {}   // define function
void Func(int) {}   // C2084 second definition
```

이 오류를 해결 하려면 중복 정의 제거 합니다.

```
// C2084b.cpp
// compile with: /c
void Func(int);
void Func(int) {}
```