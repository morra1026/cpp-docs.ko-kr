---
title: 매크로 대체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- NMAKE program, macro substitution
- macros, NMAKE
- substitution macros in NMAKE
ms.assetid: 47465cfe-fd92-49db-aebe-7c2d7ecceb73
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8f71ef2e1a8f337a4cd415169b6f9d817042f19a
ms.sourcegitcommit: d10a2382832373b900b1780e1190ab104175397f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43894397"
---
# <a name="macro-substitution"></a>매크로 대체

때 *매크로 이름* 가 호출 됩니다 때마다 *string1* 의 정의에 문자열 바뀝니다 *string2*합니다.

## <a name="syntax"></a>구문

```
$(macroname:string1=string2)
```

## <a name="remarks"></a>설명

매크로 대체 대/소문자 구분 되며 리터럴; *string1* 하 고 *string2* 매크로 호출할 수 없습니다. 대체는 원래 정의 수정 하지 않습니다. 제외한 모든 미리 정의 된 매크로의 텍스트를 대체할 수 있습니다 [ $$@ ](../build/filename-macros.md)합니다.

공백 또는 탭 앞에 콜론; 콜론 after 리터럴로 해석 됩니다. 하는 경우 *string2* 가 null 인 모든 *string1* 매크로 정의 문자열에서 삭제 됩니다.

## <a name="see-also"></a>참고 항목

[NMAKE 매크로 사용](../build/using-an-nmake-macro.md)