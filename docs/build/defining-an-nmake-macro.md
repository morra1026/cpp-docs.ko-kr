---
title: NMAKE 매크로 정의 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- macros, NMAKE
- defining NMAKE macros
- NMAKE macros, defining
ms.assetid: 45aae451-9d33-4a3d-8799-2e0cae17070d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c266a0be1c5ff16b719e9055f79b377d13ffbf3c
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45715715"
---
# <a name="defining-an-nmake-macro"></a>NMake 매크로 정의

## <a name="syntax"></a>구문

```

macroname=string
```

## <a name="remarks"></a>설명

합니다 *매크로 이름* 는 문자, 숫자 및 밑줄 (_) 최대 1,024 자의의 조합이 며 경우 중요 합니다. 합니다 *매크로 이름* 호출된 매크로 포함할 수 있습니다. 하는 경우 *매크로 이름* 구성 매크로 호출된의 완전히 null 이거나 정의 되지 않은 호출 되는 매크로 일 수 없습니다.

`string` 0 개 이상의 문자 시퀀스를 수 있습니다. Null 문자열에는 0 개의 문자 또는 공백이 나 탭만 포함 되어 있습니다. `string` 매크로 호출을 포함할 수 있습니다.

## <a name="what-do-you-want-to-know-more-about"></a>추가 정보

[매크로의 특수 문자](../build/special-characters-in-macros.md)

[Null 및 정의 되지 않은 매크로](../build/null-and-undefined-macros.md)

[매크로를 정의할 위치](../build/where-to-define-macros.md)

[매크로 정의의 우선 순위](../build/precedence-in-macro-definitions.md)

## <a name="see-also"></a>참고 항목

[매크로와 NMake](../build/macros-and-nmake.md)