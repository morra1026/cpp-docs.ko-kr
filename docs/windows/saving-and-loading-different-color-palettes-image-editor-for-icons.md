---
title: 다른 색상표 저장 및 로드(아이콘에 대한 이미지 편집기)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.image.color
- vc.editors.loadcolorpalette
helpviewer_keywords:
- color palettes [C++]
- palettes
- palettes, Image editor
- colors [C++], Image editor
- Image editor [C++], palettes
- color palettes
- Load Palette Colors dialog box [C++]
ms.assetid: 694b6346-e606-4f19-aa01-9b4ceb47f423
ms.openlocfilehash: fd2664407d33d8e3ed594921501b7f80e6c8850b
ms.sourcegitcommit: efcc8c97570ddf7631570226c700e8f6ebb6c7be
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/01/2019
ms.locfileid: "55560272"
---
# <a name="saving-and-loading-different-color-palettes-image-editor-for-icons"></a>다른 색상표 저장 및 로드(아이콘에 대한 이미지 편집기)

저장 하 고 로드할 수는 **색** 포함 하는 색상표 [색을 사용자 지정](../windows/customizing-or-changing-colors-image-editor-for-icons.md)합니다. (기본적으로 **색** 가장 최근에 사용한 팔레트는 Visual Studio를 시작 하는 경우에 자동으로 로드 됩니다.)

> [!TIP]
> 이후 합니다 **이미지** 편집기에 기본값을 복원 하려면 **색** 색상표를 기본 저장 해야 **색** 와 같은 이름으로 색상표  *standard.pal* 나 *default.pal과* 기본 설정을 쉽게 복원할 수 있도록 합니다.

사용 된 **색상표 로드** c + + 프로젝트에서 사용 하려면 특별 한 색상표 로드 대화 상자. 포함 된 다음 속성은 다음과 같습니다.

|속성|설명|
|---|---|
|**Look in**|파일 또는 폴더를 찾을 위치를 지정 합니다. 다른 위치를 선택 하 고 화살표 또는 한 수준 위로 이동 하려면 도구 모음의 폴더 아이콘을 선택 합니다.|
|**파일 이름**|열려는 파일의 이름을 입력할 공간을 제공 합니다. 이전에 열었던 파일을 빨리 찾으려면 사용 가능한 경우 드롭 다운 목록에서 파일 이름을 선택 합니다.<br/><br/>파일을 검색 하는 경우에 와일드 카드로 별표 (*)를 사용할 수 있습니다. 예를 들어 입력할 수 있습니다 \*.\* 모든 파일의 목록을 볼 수 있습니다. 예를 들어 C:\My Documents\MyColorPalette.pal 파일의 전체 경로 입력할 수도 있습니다 또는 \\\NetworkServer\MyFolder\MyColorPalette.pal 합니다.|
|**파일 형식**|표시할 파일의 목록을 표시 합니다. 색상표 (*.pal) 색상표의 기본 파일 형식입니다.|

## <a name="to-save-a-custom-colors-palette"></a>사용자 지정 색 색상표를 저장하려면

1. **이미지** 메뉴 선택 **색상표 저장**합니다.

1. 색상표를 저장할 디렉터리로 이동하고 색상표의 이름을 입력합니다.

1. **저장**을 선택합니다.

## <a name="to-load-a-custom-colors-palette"></a>사용자 지정 색 색상표를 로드하려면

1. **이미지** 메뉴 선택 **색상표 로드**합니다.

1. 에 **색상표 로드** 대화 상자 올바른 디렉터리로 이동 하 고 로드할 색상표를 선택 합니다. **색** 색상표는.pal 파일 확장명으로 저장 됩니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[색 작업](../windows/working-with-color-image-editor-for-icons.md)<br/>
[아이콘에 대한 이미지 편집기](../windows/image-editor-for-icons.md)