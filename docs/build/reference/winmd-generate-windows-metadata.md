---
title: /WINMD(Windows 메타데이터 생성)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.GenerateWindowsMetadata
ms.assetid: bcfb4901-411e-4c9e-9f78-23028b6e5fcc
ms.openlocfilehash: 83d22a0114b26f53fa9df9d2470c71cd80465d64
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57426690"
---
# <a name="winmd-generate-windows-metadata"></a>/WINMD(Windows 메타데이터 생성)

Windows 런타임 메타데이터(.winmd) 파일을 생성할 수 있게 해줍니다.

> **/WINMD**\[**:**{**NO**\|**ONLY**}]

## <a name="arguments"></a>인수

**/WINMD**<br/>
유니버설 Windows 플랫폼 앱에 대 한 기본 설정입니다. 링커가 바이너리 실행 파일 및 .winmd 메타데이터 파일을 모두 생성합니다.

**/WINMD:NO**<br/>
링커가 바이너리 실행 파일만 생성하고 .winmd 파일은 생성하지 않습니다.

**/WINMD:ONLY**<br/>
링커가 .winmd 파일만 생성하고 바이너리 실행 파일은 생성하지 않습니다.

## <a name="remarks"></a>설명

합니다 **/WINMD** 링커 옵션은 데 UWP 앱 및 Windows 런타임 구성 요소에 대 한 Windows 런타임 메타 데이터 (.winmd) 파일의 생성을 제어 합니다. .Winmd 파일은 Windows 런타임 형식 및 런타임 구성 요소를 해당 형식의 구현의 경우 메타 데이터가 포함 된 DLL의 종류입니다. 메타 데이터를 [ECMA-335](http://www.ecma-international.org/publications/standards/Ecma-335.htm) 표준입니다.

기본적으로 출력 파일의 이름 형식은 *binaryname*.winmd입니다. 다른 파일 이름을 지정 하려면 사용 합니다 [/WINMDFILE](../../build/reference/winmdfile-specify-winmd-file.md) 옵션입니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **구성 속성** > **링커** > **Windows 메타 데이터** 속성 페이지.

1. 에 **Windows 메타 데이터 생성** 드롭다운 목록 상자에서 원하는 옵션을 선택 합니다.

## <a name="see-also"></a>참고자료

[연습: 간단한 Windows 런타임 구성 요소를 만들고 JavaScript에서 호출](/windows/uwp/winrt-components/walkthrough-creating-a-simple-windows-runtime-component-and-calling-it-from-javascript)<br/>
[Microsoft Interface Definition Language 3.0 소개](/uwp/midl-3/intro)<br/>
[/WINMDFILE(winmd 파일 지정)](winmdfile-specify-winmd-file.md)<br/>
[/WINMDKEYFILE(winmd 키 파일 지정)](winmdkeyfile-specify-winmd-key-file.md)<br/>
[/WINMDKEYCONTAINER(키 컨테이너 지정)](winmdkeycontainer-specify-key-container.md)<br/>
[/WINMDDELAYSIGN(winmd에 부분적으로 서명)](winmddelaysign-partially-sign-a-winmd.md)<br/>
[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
