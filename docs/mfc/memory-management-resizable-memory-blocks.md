---
title: '메모리 관리: 크기 조정 가능한 메모리 블록 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- memory blocks [MFC], resizable
- memory [MFC], corruption
- memory allocation [MFC], memory block size
- memory blocks [MFC], allocating
- blocks [MFC], memory allocation
- resizable memory blocks [MFC]
ms.assetid: f0efe6f4-a3ed-4541-9195-51ec1291967a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 92582e4255c88b9cc78368a635b27772f2e51a30
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46443906"
---
# <a name="memory-management-resizable-memory-blocks"></a>메모리 관리: 크기 조정 가능한 메모리 블록

**새** 하 고 **삭제** 연산자를 문서에 설명 된 [메모리 관리: 예제](../mfc/memory-management-examples.md), 할당 및 크기가 고정 된 메모리 블록을 할당 취소에 적합 한 및 개체입니다. 경우에 따라 응용 프로그램 크기 조정 가능한 메모리 블록을 해야 합니다. 표준 C 런타임 라이브러리 함수를 사용 해야 [malloc](../c-runtime-library/reference/malloc.md)를 [realloc](../c-runtime-library/reference/realloc.md), 및 [무료](../c-runtime-library/reference/free.md) 힙의 크기 조정 가능한 메모리 블록을 관리할 수 있습니다.

> [!IMPORTANT]
>  혼합 합니다 **새** 하 고 **삭제** 연산자 동일한 메모리 블록의 크기 조정 가능한 메모리 할당 함수를 사용 하면 MFC의 디버그 버전에서 손상 된 메모리입니다. 사용 하지 않아야 **realloc** 사용 하 여 할당 된 메모리 블록 **새**합니다. 마찬가지로 인 메모리 블록을 하지 할당 해야 합니다 **새** 연산자를 사용 하 여 삭제 **무료**, 사용할지를 **삭제** 를사용하여할당된메모리블록에서연산자**malloc**합니다.

## <a name="see-also"></a>참고 항목

[메모리 관리: 힙 할당](../mfc/memory-management-heap-allocation.md)

