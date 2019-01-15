---
title: 힙 상수
ms.date: 11/04/2016
f1_keywords:
- _HEAPBADPTR
- _HEAPEMPTY
- _HEAPBADBEGIN
- _HEAPOK
- _HEAPBADNODE
- _HEAPEND
helpviewer_keywords:
- _HEAPOK constants
- _HEAPEND constants
- HEAPBADBEGIN constants
- _HEAPBADNODE constants
- HEAPBADNODE constants
- HEAPBADPTR constants
- _HEAPEMPTY constants
- HEAPEND constants
- HEAPOK constants
- HEAPEMPTY constants
- _HEAPBADBEGIN constants
- _HEAPBADPTR constants
- heap constants
ms.assetid: 3f751bb9-2dc4-486f-b5f5-9061c96d3754
ms.openlocfilehash: b8783a5826376a65cb71444e2d64c61b6938eab8
ms.sourcegitcommit: a1fad0a266b20b313364a74b16c9ac45d089b1e9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54220220"
---
# <a name="heap-constants"></a>힙 상수

## <a name="syntax"></a>구문

```
#include <malloc.h>
```

## <a name="remarks"></a>주의

이러한 상수는 힙의 상태를 나타내는 반환 값을 제공합니다.

|상수|의미|
|--------------|-------------|
|`_HEAPBADBEGIN`|초기 헤더 정보를 찾을 수 없거나 올바르지 않습니다.|
|`_HEAPBADNODE`|잘못된 노드가 검색되었거나 힙이 손상되었습니다.|
|`_HEAPBADPTR`|**_HEAPINFO** 구조체의 **_pentry** 필드는 힙에 대한 올바른 포인터를 포함하지 않습니다(`_heapwalk` 루틴에만 해당).|
|`_HEAPEMPTY`|힙이 초기화되지 않았습니다.|
|`_HEAPEND`|힙 끝에 성공적으로 도달했습니다(`_heapwalk` 루틴에만 해당).|
|`_HEAPOK`|힙이 일치합니다(`_heapset` 및 `_heapchk` 루틴에만 해당). 지금까지 오류가 없습니다. **_HEAPINFO** 구조체는 다음 항목에 대한 정보를 포함합니다(`_heapwalk` 루틴에만 해당).|

## <a name="see-also"></a>참고 항목

[_heapchk](../c-runtime-library/reference/heapchk.md)<br/>
[_heapset](../c-runtime-library/heapset.md)<br/>
[_heapwalk](../c-runtime-library/reference/heapwalk.md)<br/>
[전역 상수](../c-runtime-library/global-constants.md)
