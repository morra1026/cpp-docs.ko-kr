---
title: 이미지 목록의 이미지 오버레이
ms.date: 11/04/2016
helpviewer_keywords:
- overlays [MFC]
- image lists [MFC], image overlays in
- CImageList class [MFC], image overlays in
ms.assetid: aaf4e1c4-cd12-42c8-9af4-1bb458889b4e
ms.openlocfilehash: dc5c28a38d3024f3d8cbd1fa8b9fe9c1c8a09f93
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50603101"
---
# <a name="image-overlays-in-image-lists"></a>이미지 목록의 이미지 오버레이

모든 이미지 목록 ([CImageList](../mfc/reference/cimagelist-class.md)) 오버레이 마스크로 사용할 이미지의 목록을 포함 합니다. "오버레이 마스크"는 다른 이미지 위에 투명 하 게 그릴 이미지. 모든 이미지를 오버레이 마스크로 사용할 수 있습니다. 이미지 목록 당 최대 4 개의 오버레이 마스크를 지정할 수 있습니다.

사용 하 여 오버레이 마스크 목록에 이미지의 인덱스를 추가 합니다 [SetOverlayImage](../mfc/reference/cimagelist-class.md#setoverlayimage) 멤버 함수, 이미지의 인덱스 및 오버레이 마스크의 인덱스입니다. 오버레이 마스크에 대 한 인덱스는 1부터 시작 하지 않고 참고 합니다.

에 대 한 단일 호출을 사용 하 여 이미지 위에 오버레이 마스크를 그리기 `Draw`합니다. 매개 변수를 그릴 이미지의 인덱스 및 오버레이 마스크의 인덱스를 포함 합니다. 사용 해야 합니다 [INDEXTOOVERLAYMASK](/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask) 오버레이 마스크의 인덱스를 지정 하는 매크로입니다. 호출 하는 경우에 오버레이 이미지를 지정할 수 있습니다 합니다 [DrawIndirect](../mfc/reference/cimagelist-class.md#drawindirect) 멤버 함수입니다.

## <a name="see-also"></a>참고 항목

[CImageList 사용](../mfc/using-cimagelist.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

