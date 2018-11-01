---
title: 메모리 덮어쓰기 확인
ms.date: 11/04/2016
helpviewer_keywords:
- memory, overwrites
ms.assetid: da7c5d77-a267-415f-a8ab-ee5ce5bfc286
ms.openlocfilehash: ff900c7366a28d19d3b90cbd4a6d9ee732e4ce02
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50621561"
---
# <a name="checking-for-memory-overwrites"></a>메모리 덮어쓰기 확인

힙 조작 함수를 호출할 때 액세스 위반을 받게 되 면 프로그램 힙 손상 된 것입니다. 이 경우의 일반적인 증상 것입니다.

```
Access Violation in _searchseg
```

[_heapchk](../../c-runtime-library/reference/heapchk.md) 함수 디버그에 사용할 수 있고 릴리스 빌드 (Windows NT에만 해당)는 런타임 라이브러리 힙의 무결성을 확인 합니다. 사용할 수 있습니다 `_heapchk` 거의 동일한 방법으로 `AfxCheckMemory` 예를 들어, 힙 덮어쓰는 격리 하는 함수:

```
if(_heapchk()!=_HEAPOK)
   DebugBreak();
```

이 함수가 실패 하는 경우 격리 해야이 시점에서 힙 손상 되었습니다.

## <a name="see-also"></a>참고 항목

[릴리스 빌드 문제 해결](../../build/reference/fixing-release-build-problems.md)