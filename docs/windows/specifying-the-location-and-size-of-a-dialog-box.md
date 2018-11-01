---
title: 대화 상자 (c + +)의 크기와 위치를 지정합니다.
ms.date: 11/04/2016
helpviewer_keywords:
- dialog boxes [C++], size
- dialog boxes [C++], positioning
ms.assetid: 2b7c495e-6595-4cfb-9664-80b2826d0851
ms.openlocfilehash: 2c39cf5076ea38635268120da96fec6c82e23c47
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50524935"
---
# <a name="specifying-the-location-and-size-of-a-dialog-box-c"></a>대화 상자 (c + +)의 크기와 위치를 지정합니다.

위치와 크기는 c + + 대화 상자를과 같이 위치 및 안에 있는 컨트롤의 크기는 대화 단위로 측정 됩니다. 개별 컨트롤 및 대화 상자에 대 한 값은 Visual Studio 상태를 선택 하면 표시줄의 오른쪽 아래에 나타납니다.

세 가지 속성에 설정할 수 있는 합니다 [속성 창](/visualstudio/ide/reference/properties-window) 대화 상자가 화면 표시를 지정 합니다. 합니다 **Center** 속성은 부울; 값을 설정 하는 경우 **True**, 대화 상자 화면 중앙에 항상 표시 됩니다. 설정 하면 **False**를 설정할 수 있습니다 합니다 **XPos** 및 **YPos** 화면 대화 상자를 표시할 위치를 명시적으로 정의 하는 속성입니다. 위치 속성으로 정의 된 보기 영역의 왼쪽 위 모서리에서 오프셋된 값은 `{X=0, Y=0}`합니다. 위치를 기준으로 합니다 **Absolute Align** 속성: 경우 **True**, 좌표는 화면을 기준으로 하는 경우 **False**, 대화 상자를 기준으로 좌표는 소유자 창입니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리 되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대 한 내용은 참조 하세요 [데스크톱 앱에 대 한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)합니다. 전역화 및 지역화 관리 되는 앱의 리소스에 대 한 내용은 참조 하세요 [Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤](../mfc/controls-mfc.md)