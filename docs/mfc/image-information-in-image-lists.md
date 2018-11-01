---
title: 이미지 목록의 이미지 정보
ms.date: 11/04/2016
helpviewer_keywords:
- CImageList class [MFC], image information in
- image lists [MFC], image information in
ms.assetid: 73c41543-fa91-405d-b15b-0feffa6a72c1
ms.openlocfilehash: 60cac844a83e898719cc67776b01eb2b0ffe4896
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50440225"
---
# <a name="image-information-in-image-lists"></a>이미지 목록의 이미지 정보

[CImageList](../mfc/reference/cimagelist-class.md) 다양 한 이미지 목록에서 정보를 검색 하는 함수가 포함 되어 있습니다. 합니다 [GetImageInfo](../mfc/reference/cimagelist-class.md#getimageinfo) 멤버 함수는 채웁니다는 `IMAGEINFO` 단일 이미지를 이미지와 마스크 비트맵, 색상 평면 및 픽셀 당 비트 수 및 경계 사각형의 핸들을 포함 하는 방법에 대 한 정보로 구조체 이미지 비트맵 내 이미지입니다. 이미지에 대 한 비트맵을 직접 조작 하려면이 정보를 사용할 수 있습니다.

합니다 [GetImageCount](../mfc/reference/cimagelist-class.md#getimagecount) 멤버 함수는 이미지 목록의 이미지 개수를 검색 합니다.

이미지 및 이미지 목록에 마스크를 사용 하 여 기반 아이콘을 만들 수 있습니다 합니다 [ExtractIcon](../mfc/reference/cimagelist-class.md#extracticon) 멤버 함수입니다. 함수를 새 아이콘의 핸들을 반환합니다.

## <a name="see-also"></a>참고 항목

[CImageList 사용](../mfc/using-cimagelist.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

