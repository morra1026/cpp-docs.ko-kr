---
title: 컴파일러 경고 (수준 1) C4788 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4788
dev_langs:
- C++
helpviewer_keywords:
- C4788
ms.assetid: 47d75bda-f833-4bdd-93a0-a134df0cd303
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1c8a6ad1aa3ae17944b8c2a292d484d55c24d9cd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051739"
---
# <a name="compiler-warning-level-1-c4788"></a>컴파일러 경고(수준 1) C4788

'identifier': 식별자 'number' 자로 잘렸습니다.

컴파일러는 함수 이름을 사용할 수 있는 최대 길이 제한 합니다. 일부 텍스트를 사용 하 여 함수 이름을 추가 하 여 작은 함수 이름을 형성 컴파일러 funclets EH/SEH 코드를 생성할 때 "__catch를 선택 예를 들어", "\__unwind", 또는 다른 문자열입니다.

결과 작은 함수 이름이 너무 길어질 수 있습니다 및 컴파일러를 잘라 C4788를 생성 합니다.

이 경고를 해결 하려면 원래 함수 이름을 단축 합니다. 함수는 c + + 템플릿 함수 또는 메서드 이면 이름 부분에 대 한 typedef를 사용 합니다. 예를 들어:

```
C1<x, y, z<T>>::C2<a,b,c>::f
```

으로 바꿀 수 있습니다.

```
typedef C1<x, y, z<T>>::C2<a,b,c> new_class ;
new_class::f
```

이 경고는 x64 에서만 발생 컴파일러.