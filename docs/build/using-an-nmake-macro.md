---
title: NMAKE 매크로 사용
ms.date: 11/04/2016
helpviewer_keywords:
- macros, NMAKE
- NMAKE macros, using
ms.assetid: 95c87fbc-76e6-48c0-8536-9bfe179f328e
ms.openlocfilehash: 9d8ff76e1e730b65db363749797ef9ae2062adab
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50645083"
---
# <a name="using-an-nmake-macro"></a>NMAKE 매크로 사용

매크로 사용 하려면 해당 이름을 앞에 달러 기호 ($)에 다음과 같이 괄호로 묶습니다.

## <a name="syntax"></a>구문

```
$(macroname)
```

## <a name="remarks"></a>설명

공백이 허용 됩니다. 괄호를 사용할 경우 *매크로 이름* 단일 문자입니다. 정의 문자열 $ 바꿉니다 (*매크로 이름*);는 정의 되지 않은 매크로 null 문자열로 바뀝니다.

## <a name="what-do-you-want-to-know-more-about"></a>추가 정보

[매크로 대체](../build/macro-substitution.md)

## <a name="see-also"></a>참고 항목

[매크로와 NMake](../build/macros-and-nmake.md)