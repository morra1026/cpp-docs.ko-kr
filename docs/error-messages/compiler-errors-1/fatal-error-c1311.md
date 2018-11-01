---
title: 심각한 오류 C1311
ms.date: 11/04/2016
f1_keywords:
- C1311
helpviewer_keywords:
- C1311
ms.assetid: 6590a06c-ce9d-4f17-8f62-c809343143b8
ms.openlocfilehash: ba2b797c9bf521533e7c2ccff8d358b6216d392f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50637907"
---
# <a name="fatal-error-c1311"></a>심각한 오류 C1311

COFF 형식은 'var' 숫자 바이트의 주소를 사용 하 여 정적으로 초기화할 수 없습니다.

4 바이트 미만인 저장소 형식은 변수에 값인 컴파일 타임에 알려지지 않은 주소를 정적으로 할당할 수 없습니다.

이 오류 코드이 고 그렇지 않으면 하는 유효한 c + +입니다.

다음 코드 예제는 C1311을 일으킬 수 있는 한 가지 조건을 보여줍니다.

```
char c = (char)"Hello, world";   // C1311
char *d = (char*)"Hello, world";   // OK
```