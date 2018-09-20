---
title: 할당 및 창 메모리 할당 취소 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- memory allocation, window objects
- memory deallocation
- storage for window objects [MFC]
- memory deallocation, window memory
- window objects [MFC], deallocating memory for
- storage for window objects [MFC], allocating
ms.assetid: 7c962539-8461-4846-b5ca-fe3b15c313dc
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 149a8e860913515551fc85be9b49675856d7e129
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46415197"
---
# <a name="allocating-and-deallocating-window-memory"></a>창 메모리 할당 및 할당 취소

C + +를 사용 하지 마세요 **삭제** 프레임 창 또는 보기를 제거 하는 연산자입니다. 대신, 호출 된 `CWnd` 멤버 함수 `DestroyWindow`합니다. 프레임 창 따라서 할당 되는 연산자를 사용 하 여 힙에 **새**합니다. 프레임 창 또는 전역 스택 프레임에 할당할 때 주의 해야 합니다. 다른 windows 가능 하면 스택 프레임에 할당 되어야 합니다.

## <a name="what-do-you-want-to-know-more-about"></a>자세히 알아보려는 항목

- [창 만들기](../mfc/creating-windows.md)

- [창 소멸 시퀀스](../mfc/window-destruction-sequence.md)

- [해당 HWND에서에서 CWnd 분리](../mfc/detaching-a-cwnd-from-its-hwnd.md)

## <a name="see-also"></a>참고 항목

[창 개체 제거](../mfc/destroying-window-objects.md)

