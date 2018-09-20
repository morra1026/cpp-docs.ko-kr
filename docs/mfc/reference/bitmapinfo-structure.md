---
title: BITMAPINFO 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- BITMAPINFO
dev_langs:
- C++
helpviewer_keywords:
- BITMAPINFO structure [MFC]
ms.assetid: a00caa49-e4df-419f-89a7-ab03c13a1b5b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9e114af97385241674cf9baa4f8d9883acdadef3
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46405959"
---
# <a name="bitmapinfo-structure"></a>BITMAPINFO 구조체

`BITMAPINFO` 차원 및 Windows 장치 독립적 비트맵이 (DIB)에 대 한 색 정보 구조를 정의 합니다.

## <a name="syntax"></a>구문

```
typedef struct tagBITMAPINFO {
    BITMAPINFOHEADER bmiHeader;
    RGBQUAD bmiColors[1];
} BITMAPINFO;
```

#### <a name="parameters"></a>매개 변수

*bmiHeader*<br/>
지정 된 [BITMAPINFOHEADER](https://msdn.microsoft.com/library/windows/desktop/dd183376) 차원 및 장치 독립적 비트맵의 색 형식에 대 한 정보를 포함 하는 구조입니다.

*bmiColors*<br/>
사용자 지정 [RGBQUAD](/windows/desktop/api/wingdi/ns-wingdi-tagrgbquad) 또는 비트맵의 색을 정의 하는 DWORD 데이터 형식입니다.

## <a name="remarks"></a>설명

장치 독립적 비트맵 두 부분으로 이루어져:는 `BITMAPINFO` 차원 및 비트맵의 색 및 비트맵의 픽셀을 지정 하는 바이트 배열을 설명 하는 구조입니다. 배열에 있는 비트를 함께 압축 됩니다 있지만 0으로 끝나는 각 스캐닝선 패딩해야를 **긴** 경계입니다. 높이 양수인 경우 비트맵의 원점은 왼쪽 아래 모퉁이입니다. 높이가 음수 이면 원점은 왼쪽 위 모퉁이입니다.

A *압축된 비트맵* 은 비트맵 바이트 배열 바로 뒤의 `BITMAPINFO` 구조입니다. 압축 된 비트맵은 단일 포인터에 의해 참조 됩니다.

에 대 한 자세한 내용은 합니다 `BITMAPINFO` 구조체 및 값의 멤버에 대 한 적절 한는 `BITMAPINFOHEADER` 및 `RGBQUAD` 구조는 Windows SDK 설명서의 다음 항목을 참조 합니다.

- [BITMAPINFO 구조체](/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo)

- [BITMAPINFOHEADER](https://msdn.microsoft.com/library/windows/desktop/dd183376) 구조

- [RGBQUAD](/windows/desktop/api/wingdi/ns-wingdi-tagrgbquad) 구조

## <a name="requirements"></a>요구 사항

**헤더:** wingdi.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CBrush::CreateDIBPatternBrush](../../mfc/reference/cbrush-class.md#createdibpatternbrush)<br/>
[BITMAPINFOHEADER](https://msdn.microsoft.com/library/windows/desktop/dd183376)<br/>
[RGBQUAD](/windows/desktop/api/wingdi/ns-wingdi-tagrgbquad)

