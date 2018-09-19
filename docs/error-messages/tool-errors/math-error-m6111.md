---
title: 수학 오류 M6111 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- M6111
dev_langs:
- C++
helpviewer_keywords:
- M6111
ms.assetid: c0fc13f8-33c8-4e3f-a440-126cc623441b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 95a55ec6b7cdf0b6e4c15bd283dde77c610698fa
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074827"
---
# <a name="math-error-m6111"></a>수학 오류 M6111

언더플로 스택

부동 소수점 연산 8087/287 387 프로세서 또는 에뮬레이터에는 스택 언더플로 했습니다.

이 오류는 호출 하 여 자주 발생을 `long double` 함수 값을 반환 하지 않습니다. 예를 들어, 다음이 오류를 생성 컴파일 및 실행 하는 경우:

```
long double ld() {};
main ()
{
  ld();
}
```

프로그램은 139 종료 코드로 종료 됩니다.