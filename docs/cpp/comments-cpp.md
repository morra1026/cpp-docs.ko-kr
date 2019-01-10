---
title: 주석 (c + +)
ms.date: 11/04/2016
helpviewer_keywords:
- code comments, C++
- comments, documenting code
- comments, C++ code
- white space, C++ comments
ms.assetid: 6fcb906c-c264-4083-84bc-373800b2e514
ms.openlocfilehash: a90d9d37e69cb2e8be4ab18f77026fdce1221307
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50506108"
---
# <a name="comments-c"></a>주석 (c + +)

메모는 프로그래머에 게 유용 하지만 컴파일러에서 무시 하는 텍스트입니다. 일반적으로 주석은 나중에 참조할 수에 대 한 코드에 주석을 사용 합니다. 컴파일러는 공백 처리 합니다. 비활성; 특정 코드 줄 수 있도록 주석을 테스트를 사용할 수 있습니다. 그러나 `#if` / `#endif` 전처리기 지시문에 더 적합 한이 주석이 포함 된 코드를 둘러쌀 수 있습니다 하지만 주석 중첩할 수 없습니다.

C++ 주석은 다음 방법 중 하나로 기록됩니다.

- 합니다 `/*` (슬래시, 별표) 뒤에 임의의 문자 시퀀스입니다 (줄 바꿈 포함) 뒤에 문자를 `*/` 문자입니다. 이 구문은 ANSI C.와 동일

- `//`(슬래시 두 개) 다음에 임의의 문자들이 나옵니다. 백슬래시가 바로 앞에 오지 않는 새 줄은 이러한 형식의 주석을 종료합니다. 따라서 일반적으로 "한 줄 주석"이라고 합니다.

주석 문자(`/*`, `*/`, 및 `//`)는 문자 상수, 문자열 리터럴 또는 주석 안에서 특별한 의미가 없습니다. 따라서 첫 번째 구문을 사용하는 주석은 중첩할 수 없습니다.

## <a name="see-also"></a>참고 항목

[어휘 규칙](../cpp/lexical-conventions.md)