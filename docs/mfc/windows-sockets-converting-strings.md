---
title: 'Windows 소켓: 문자열 변환 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- Windows Sockets [MFC], multibyte character string conversion
- sockets [MFC], multibyte character string conversion issues
- string conversion, multibyte character strings
ms.assetid: 9df522b5-6b23-41e0-bb96-e4e623baf141
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 6b23d2149659cdad320a58bdff0f42ba113b5696
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46378942"
---
# <a name="windows-sockets-converting-strings"></a>Windows 소켓: 문자열 변환

이 문서 및 두 개의 참조 문서에서는 Windows 소켓 프로그래밍의 몇 가지 문제를 설명합니다. 이 문서에서는 문자열 변환에 대해 설명 합니다. 기타 문제에 나와 [Windows 소켓: 차단](../mfc/windows-sockets-blocking.md) 하 고 [Windows 소켓: 바이트 순서](../mfc/windows-sockets-byte-ordering.md)합니다.

사용 하거나 클래스에서 파생 되는 경우 [CAsyncSocket](../mfc/reference/casyncsocket-class.md), 이러한 문제를 직접 관리 해야 합니다. 사용 하거나 클래스에서 파생 되는 경우 [CSocket](../mfc/reference/csocket-class.md), MFC를 관리 합니다.

## <a name="converting-strings"></a>문자열 변환

유니코드 또는 멀티 바이트 문자 집합 (MBCS)의 경우와 같은 다양 한 와이드 문자 형식으로 저장 된 문자열을 사용 하는 응용 프로그램 간에 통신 하거나 중와 ANSI 문자열을 사용 하 여 응용 프로그램 간의 변환을 관리 해야 하는 경우 직접 `CAsyncSocket`입니다. 합니다 `CArchive` 사용 되는 개체를 `CSocket` 개체는 이러한 변환 기능을 통해 클래스의 관리 [CString](../atl-mfc-shared/reference/cstringt-class.md)합니다. 자세한 내용은 Windows SDK에는 Windows Sockets 사양을 참조 하세요.

자세한 내용은 다음을 참조하세요.

- [Windows 소켓: CAsyncSocket 클래스 사용](../mfc/windows-sockets-using-class-casyncsocket.md)

- [Windows 소켓: 소켓과 아카이브 함께 사용](../mfc/windows-sockets-using-sockets-with-archives.md)

- [Windows 소켓: 백그라운드](../mfc/windows-sockets-background.md)

- [Windows 소켓: 스트림 소켓](../mfc/windows-sockets-stream-sockets.md)

- [Windows 소켓: 데이터그램 소켓](../mfc/windows-sockets-datagram-sockets.md)

## <a name="see-also"></a>참고 항목

[MFC의 Windows 소켓](../mfc/windows-sockets-in-mfc.md)

