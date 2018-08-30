---
title: 컴파일러 경고 (수준 1) C4325 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4325
dev_langs:
- C++
helpviewer_keywords:
- C4325
ms.assetid: 8127a08c-d626-481b-aa7b-04a3fdc9a9ec
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cd265938afb51cc402dc84f38b7e95188c6292a7
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43197487"
---
# <a name="compiler-warning-level-1-c4325"></a>컴파일러 경고(수준 1) C4325

> 표준 섹션에 대 한 특성 '*섹션*' 무시

## <a name="remarks"></a>설명

표준 섹션의 특성을 변경할 수 없습니다. 예를 들어:

```cpp
#pragma section(".sdata", long)
```

이 덮어씁니다를 `.sdata` 를 사용 하는 표준 섹션의 **짧은** 데이터 형식을 **긴** 데이터 형식.

표준 섹션 변경할 수 없습니다 특성 포함

- .data

- .sdata

- .bss

- .sbss

- .text

- .const

- .sconst

- .rdata

- .srdata

추가 섹션은 나중에 추가할 수 있습니다.

## <a name="see-also"></a>참고자료

[section](../../preprocessor/section.md)