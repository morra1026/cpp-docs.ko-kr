---
title: 식 계산기 오류 CXX0064 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0064
dev_langs:
- C++
helpviewer_keywords:
- CAN0064
- CXX0064
ms.assetid: aa509e71-0616-41ca-a94e-6c376b041e57
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b16133484af5a2225f79c5d293a2c8edd948bdb2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46025895"
---
# <a name="expression-evaluator-error-cxx0064"></a>식 계산기 오류 CXX0064

바인딩된 가상 멤버 함수에 중단점을 설정할 수 없습니다.

와 같은 개체에 대 한 포인터를 통해 가상 멤버 함수에 중단점 설정 된:

```
pClass->vfunc( int );
```

와 같은 클래스를 입력 하 여 가상 함수에 중단점을 설정할 수 있습니다.

```
Class::vfunc( int );
```

이 오류는 can0064와 동일 합니다.