---
title: 컴파일러 오류 C2632 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2632
dev_langs:
- C++
helpviewer_keywords:
- C2632
ms.assetid: b15a6b1b-42d2-4e1b-8660-e6bfde61052d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7bf03c35c60bebb52c94ed04cca2349f35c06fbc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46093652"
---
# <a name="compiler-error-c2632"></a>컴파일러 오류 C2632

'type1' 'type2' 뒤에 올바르지 않습니다.

이 오류는 두 가지 형식 지정자 사이 코드가 누락 된 경우 발생할 수 있습니다.

다음 샘플에서는 C2632 오류가 생성 됩니다.

```
// C2632.cpp
int float i;   // C2632
```

이 오류 Visual Studio.NET 2003에 대해 수행한 컴파일러 규칙 작업의 결과로 생성 될 수도 있습니다. `bool` 이제 적절 한 형식이입니다. 이전 버전에서는 `bool` typedef에서 되었으며 해당 이름의 식별자를 만들 수 있습니다.

다음 샘플에서는 C2632 오류가 생성 됩니다.

```
// C2632_2.cpp
// compile with: /LD
void f(int bool);   // C2632
```

이 오류 코드는 Visual Studio.NET 2003 및 Visual Studio.NET 버전 모두 Visual c + +에서 유효한를 해결 하려면 식별자를 이름을 바꿉니다.