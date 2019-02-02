---
title: 색 사용자 지정 또는 변경(아이콘에 대한 이미지 편집기)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.customcolorselector
helpviewer_keywords:
- dithered color, Image editor
- Custom Color Selector dialog box [C++]
- Image editor [C++], Colors Palette
- colors [C++], image
- bitmaps [C++], colors
- images [C++], colors
- HSL values
- Colors Palette, Image editor
- RGB color values
- Adjust Colors command [C++]
- Image editor [C++], dithered color
ms.assetid: e58f6b32-f435-4d9a-a570-7569433661ae
ms.openlocfilehash: 7ab353ad0aa22c74eeba58e9310d9bc0f8d5a832
ms.sourcegitcommit: efcc8c97570ddf7631570226c700e8f6ebb6c7be
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/01/2019
ms.locfileid: "55560285"
---
# <a name="customizing-or-changing-colors-image-editor-for-icons"></a>색 사용자 지정 또는 변경(아이콘에 대한 이미지 편집기)

합니다 **이미지** 편집자 [색상표](../windows/colors-window-image-editor-for-icons.md) 처음에 16 개의 표준 색을 표시 합니다. 표시 된 색을 사용 하 여 사용자 지정 색도 만들 수 있습니다. 그런 다음 [저장 하 고 사용자 지정된 색 색상표 로드](../windows/saving-and-loading-different-color-palettes-image-editor-for-icons.md)합니다.

합니다 **사용자 지정 색 선택** 대화 상자를 사용 하면 이미지에 사용할 색을 사용자 지정할 수 있습니다. 포함 된 다음 속성은 다음과 같습니다.

|속성|설명|
|---|---|
|**그라데이션 색 디스플레이**|선택한 색의 값을 변경 합니다. 십자선을 변경 하려면 색에 배치 합니다. 그런 다음 슬라이더를 위나 아래로 이동 변경 명도 또는 색의 RGB 값.|
|**명도 막대**|선택한 색의 명도 설정 합니다 **그라데이션 색 디스플레이** 상자입니다. 밝기 모음을 흰색 화살표를 끌어서 선택 또는 작은 중단 되었습니다. 합니다 **Color** 선택한 색 및 효과 설정한 명도를 상자에 표시 됩니다.|
|**색**|정의 하는 색의 색상 (컬러 휠 값)를 나열 합니다. 값 범위는 0부터 240 여기서 0은 빨강, 60은 노란색, 120은 녹색, 180은 녹청, 200은 자홍, 240는 파란색입니다.|
|**Hue**|정의 하는 색의 색상 (컬러 휠 값)를 나열 합니다. 값 범위는 0부터 240 여기서 0은 빨강, 60은 노란색, 120은 녹색, 180은 녹청, 200은 자홍, 240는 파란색입니다.|
|**Sat**|정의 하는 색의 채도 값을 지정 합니다. 채도 색을 지정한 색상의 크기입니다. 값은 0에서 240 까지입니다.|
|**Lum**|정의 하는 색의 명도 (밝기)를 나열 합니다. 값은 0에서 240 까지입니다.|
|**빨간색**|정의 하는 색의 빨강 값을 지정 합니다. 0에서 255 사이의 값입니다.|
|**녹색**|정의 하는 색의 녹색 값을 지정 합니다. 0에서 255 사이의 값입니다.|
|**Blue**|정의 하는 색의 파랑 값을 지정 합니다. 0에서 255 사이의 값입니다.|

## <a name="to-change-colors-on-the-colors-palette"></a>색상표에서 색을 변경하려면

1. **이미지** 메뉴 선택 **색 조정**합니다.

1. 에 **사용자 지정 색 선택** 대화 상자, 적절 한 텍스트 상자에 RGB 또는 HSL 값을 입력 하 여 색을 정의 하거나에서 색을 선택 합니다 **그라데이션 색 디스플레이** 상자입니다.

1. 슬라이더를 이동 하 여 명도 설정 합니다 **명도** 모음입니다.

1. 많은 사용자 지정 색이 디더링됩니다. 디더링된 색에 가장 가까운 단색을 원하면 두 번 클릭 합니다 **Color** 상자입니다.

   디더링된 색을 원하는 나중에에서 슬라이더를 이동 합니다 **명도** 가로 막대형 또는 십자에서 이동를 **그라데이션 색 디스플레이** 상자 하 여 디더링을 복원 합니다.

1. 선택 **확인** 새로운 색을 추가 합니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[색 작업](../windows/working-with-color-image-editor-for-icons.md)<br/>
[이미지 메뉴](../windows/image-menu-image-editor-for-icons.md)<br/>
[색상 창](../windows/colors-window-image-editor-for-icons.md)