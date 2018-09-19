---
title: 문장 부호 (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- devlang-cpp
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- punctuators [C++]
ms.assetid: 1521564c-a977-488a-9490-068079897592
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 438b3f0469d1e8426b1e0ec2a19a63d1ae63c041
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039272"
---
# <a name="punctuators-c"></a>문장 부호 (c + +)

C++의 문장 부호는 컴파일러에서 구문 및 의미 체계를 의미하지만 스스로 값을 생성하는 연산을 지정하지 않습니다. 또한 일부 단독 또는 조합 문장 기호는 C++ 연산자가 될 수도 있고 전처리기에 중요할 수도 있습니다.

다음 문자는 모두 문장 부호로 간주됩니다.

```
! % ^ & * ( ) - + = { } | ~
[ ] \ ; ' : " < > ? , . / #
```

문장 부호 **[]**, **()**, 및 **{}** 뒤에 야 [변환 단계](../preprocessor/phases-of-translation.md) 4입니다.

## <a name="see-also"></a>참고자료

[어휘 규칙](../cpp/lexical-conventions.md)