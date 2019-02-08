---
title: 매니페스트 리소스 (c + +)
ms.date: 11/04/2016
helpviewer_keywords:
- manifest resources [C++]
- resources [C++], manifest
- resources [C++], opening
ms.assetid: 8615334c-22a0-44c0-93e0-5924528c9917
ms.openlocfilehash: 2d135cb2d512313f107eef7e95ec90d7972b68b4
ms.sourcegitcommit: bd637e9c39650cfd530520ea978a22fa4caa0e42
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55850192"
---
# <a name="manifest-resources-c"></a>매니페스트 리소스 (c + +)

C + + 데스크톱 프로젝트에서 매니페스트 리소스는 응용 프로그램에서 사용 하는 종속성을 설명 하는 XML 파일입니다. 예를 들어 Visual Studio의 MFC 마법사에서 생성되는 매니페스트 파일은 애플리케이션이 Windows 공용 컨트롤 DLL 버전 5.0 또는 6.0 중 어느 것을 사용해야 하는지 정의합니다.

```xml
<description>Your app description here</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="X86"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
```

Windows XP 또는 Windows Vista 애플리케이션의 경우, 매니페스트 리소스는 애플리케이션이 최신 버전(위에 나온 대로 v6.0)의 Windows 공용 컨트롤을 사용하도록 지정할 뿐만 아니라 [Syslink 컨트롤](/windows/desktop/Controls/syslink-overview)도 지원합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다.

버전을 보려면 매니페스트 리소스에 포함 된 정보를 입력을 XML 뷰어 또는 Visual Studio 텍스트 편집기에서 파일을 열 수 있습니다. [리소스 뷰](../windows/resource-view-window.md)에서 매니페스트 리소스를 열면 리소스가 이진 형식으로 열립니다. 쉬운 형식에서 매니페스트 리소스의 콘텐츠를 보려는 리소스를 열어야 **솔루션 탐색기**합니다.

## <a name="to-open-a-manifest-resource-in-the-text-editor"></a>텍스트 편집기에서 매니페스트 리소스를 열려면

1. 프로젝트를 열고 사용 하 여 **솔루션 탐색기**를 확장 합니다 **리소스 파일** 폴더입니다.

1. .manifest 파일을 두 번 클릭합니다.

   매니페스트 리소스 열립니다는 **텍스트 편집기**합니다.

## <a name="to-open-a-manifest-resource-in-another-editor"></a>다른 편집기에서 매니페스트 리소스를 열려면

1. **솔루션 탐색기**.manifest 파일을 마우스 오른쪽 단추로 클릭 하 고 선택 **연결 프로그램...**  바로 가기 메뉴에서.

1. 에 **연결** 대화 상자에서 사용 하 고 선택 하려는 편집기를 지정한 **오픈**합니다.

## <a name="limitations"></a>제한 사항

모듈별로 매니페스트 리소스를 하나만 사용할 수 있습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[컨트롤](../mfc/controls-mfc.md)<br/>
[리소스 파일 작업](../windows/working-with-resource-files.md)