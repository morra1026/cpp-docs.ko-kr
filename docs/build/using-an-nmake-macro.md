---
title: NMAKE 매크로 사용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- macros, NMAKE
- NMAKE macros, using
ms.assetid: 95c87fbc-76e6-48c0-8536-9bfe179f328e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e0b68a5f3128b5d3780895f8080411819ed9b538
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45712597"
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