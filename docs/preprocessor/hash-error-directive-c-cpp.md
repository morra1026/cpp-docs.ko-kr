---
title: '#오류 지시문 (C/c + +)'
ms.date: 11/04/2016
f1_keywords:
- '#error'
helpviewer_keywords:
- '#error directive'
- preprocessor, directives
- error directive (#error directive)
ms.assetid: d550a802-ff19-4347-9597-688935d23b2b
ms.openlocfilehash: c83fc7ef8135ee0cba37a956df47bcab0f796007
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50447816"
---
# <a name="error-directive-cc"></a>#error 지시문 (C/C++)
합니다 **#error** 지시문 컴파일 타임에 사용자 지정 오류 메시지를 내보내는 하 고 컴파일을 종료 합니다.

## <a name="syntax"></a>구문

```
#errortoken-string
```

## <a name="remarks"></a>설명

이 지시문이 생성 하는 오류 메시지에 포함 된 *토큰 문자열* 매개 변수입니다. 합니다 *토큰 문자열* 매개 변수는 매크로 확장이 적용 되지 않습니다. 이 지시어는 불일치를 프로그램의 개발자 또는 제약 조건 위반을 알리기 위한 전처리 중 가장 유용 합니다. 다음 예에서는 전처리 도중 처리 하는 오류를 보여 줍니다.

```
#if !defined(__cplusplus)
#error C++ compiler required.
#endif
```

## <a name="see-also"></a>참고 항목

[전처리기 지시문](../preprocessor/preprocessor-directives.md)