---
title: 리소스 파일(C++)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.resource
helpviewer_keywords:
- resources [C++]
- .rc files [C++]
- resource files [C++]
- resource script files [C++]
- resource script files [C++], Win-32 based applications
- resource script files [C++], files updated when editing resources
- resources [C++], types of resource files
- rct files [C++]
- rc files [C++]
- resource files [C++], types of
- .rct files [C++]
- resource script files [C++], unsupported types
- manifest resources [C++]
- resources [C++], manifest
- resources [C++], opening
- file types [C++], for resources
- resources [C++], editing
- files [C++], editable types
- resource editing
ms.assetid: 4d2b6fcc-07cf-4289-be87-83a60f69533c
ms.openlocfilehash: 65500644b70841f372edcc6911edefc6c7b9f432
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152692"
---
# <a name="resource-files-c"></a>리소스 파일(C++)

> [!NOTE]
> 이 자료는 Windows 데스크톱 애플리케이션에 적용됩니다. 유니버설 Windows 플랫폼 앱의 리소스에 대한 자세한 내용은 [앱 리소스 정의](/windows/uwp/app-resources/)를 참조하세요.
>
> 관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 리소스 지역화에 대한 내용은 [Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)를 참조하세요.
>
> .NET 프로그래밍 언어의 프로젝트는 리소스 스크립트 파일을 사용하지 않으므로 **솔루션 탐색기**에서 리소스를 열어야 합니다. 관리되는 프로젝트에서 리소스 파일로 작업하려면 [이미지 편집기](../windows/image-editor-for-icons.md) 및 [바이너리 편집기](binary-editor.md)를 사용할 수 있습니다. 편집할 관리되는 리소스는 연결된 리소스여야 합니다. Visual Studio 리소스 편집기에서는 포함된 리소스를 편집할 수 없습니다.

"리소스 파일"이라는 용어는 다음을 포함한 여러 파일 형식을 나타낼 수 있습니다.

- 프로그램의 리소스 스크립트(.rc) 파일

- 리소스 템플릿(.rct) 파일

- .rc 파일에서 참조되는 비트맵, 아이콘 또는 커서 파일과 같이 독립 실행형 파일로 존재하는 개별 리소스

- .rc 파일에서 참조되며 개발 환경에서 생성된 헤더 파일(예: Resource.h)

리소스에 있습니다. 또한 [다른 파일 형식](../windows/editable-file-types-for-resources.md) .exe,.dll 및.res 파일과 같은 합니다. 현재 프로젝트의 일부가 아닌 스냅숏과 프로젝트 내에서 리소스 및 리소스 파일을 사용 하 여 작업할 수 있습니다. Visual Studio의 개발 환경에서 작성 하지 않은 리소스 파일을 사용 하 여 작업할 수 있습니다. 예를 들어 다음 작업을 할 수 있습니다.

- 중첩되어 조건부로 포함된 리소스 파일에 대한 작업

- 기존 리소스 업데이트 또는 Visual C++ 형식으로 변환

- 현재 리소스 파일에서 그래픽 리소스 가져오기 또는 내보내기

- 개발 환경에서 수정할 수 없는 공유 또는 읽기 전용 식별자(기호) 포함

- 편집할 필요가 (또는 편집할 수 없습니다) 현재 프로젝트에서 여러 프로젝트 간에 공유 리소스와 같은 실행 파일 (.exe) 파일에서 리소스를 포함 합니다.

- 개발 환경에서 지원하지 않는 리소스 형식 포함

다음 형식의 파일을 열고 포함 하는 리소스를 편집할 수 있습니다.

|파일 이름|설명|
|---------------|-----------------|
|.rc|리소스 스크립트 파일입니다.|
|.rct|리소스 템플릿 파일입니다.|
|.res|리소스 파일입니다.|
|.resx|관리되는 리소스 파일입니다.|
|.exe|실행 파일입니다.|
|.dll|동적 연결 라이브러리 파일입니다.|
|.bmp, .ico, .dib, and .cur|비트맵, 아이콘, 도구 모음 및 커서 파일입니다.|

Visual Studio 환경을 사용 하며 리소스 편집 세션 중 다음 표에 표시 된 파일에 영향을 줍니다.

|파일 이름|설명|
|---------------|-----------------|
|Resource.h|개발 환경에서 생성된 헤더 파일로, 기호 정의를 포함합니다. (소스 제어에이 파일을 포함 합니다.)|
|Filename.aps|현재 리소스 스크립트 파일의 이진 버전으로, 빠른 로드를 위해 사용됩니다.<br /><br /> 리소스 편집기에서.rc 또는 resource.h 파일을 읽을 직접 하지 않습니다. 리소스 컴파일러는 리소스 편집기에서 사용되는 이러한 파일을 .aps 파일로 컴파일합니다. 이 파일은 컴파일 단계이며 기호화된 데이터만 저장합니다. 일반적인 컴파일 프로세스를 따라 없는 (예: 주석) 기호화 된 정보에는 컴파일 프로세스 중 삭제 됩니다. .aps 파일이 .rc 파일과 동기화되지 않을 때마다 .rc 파일이 다시 생성됩니다. 예를 들어 저장하면 리소스 편집기에서 .rc 파일 및 resource.h 파일을 덮어씁니다. 리소스 자체의 모든 변경 내용은 .rc 파일에 통합된 상태로 유지되지만 주석은 .rc 파일을 덮어쓰면 항상 손실됩니다. 주석을 유지 하는 방법에 대 한 자세한 내용은 [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)합니다. (일반적으로 있습니다 포함 하지 않아야.aps 파일이 소스 제어에.)|
|.rc|현재 프로젝트의 리소스에 대한 스크립트가 포함된 리소스 스크립트 파일입니다. 저장할 때마다 .aps 파일이 이 파일을 덮어씁니다. (소스 제어에이 파일을 포함 합니다.)|

이 섹션에서는 설명 하는 방법.

- [리소스 만들기](../windows/how-to-create-a-resource-script-file.md)

- [리소스 관리](../windows/how-to-copy-resources.md)

- [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)

## <a name="manifest-resources"></a>매니페스트 리소스

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

Windows XP 또는 Windows Vista 응용 프로그램의 경우 매니페스트 리소스 뿐만 아니라 지정 하 고 응용 프로그램, 위와 같이 최신 버전의 Windows 공용 컨트롤, v6.0 사용 하 여 있지만 지원 합니다 [Syslink 컨트롤](/windows/desktop/Controls/syslink-overview)합니다.

버전을 보려면 매니페스트 리소스에 포함 된 정보를 입력을 XML 뷰어 또는 Visual Studio 텍스트 편집기에서 파일을 열 수 있습니다. [리소스 뷰](../windows/resource-view-window.md)에서 매니페스트 리소스를 열면 리소스가 이진 형식으로 열립니다. 쉬운 형식에서 매니페스트 리소스의 콘텐츠를 보려는 리소스를 열어야 **솔루션 탐색기**합니다.

매니페스트 리소스를 열려면 다음 단계에서 선택 합니다.

- 프로젝트를 열고 사용 하 여 텍스트 편집기에 대 한 **솔루션 탐색기**를 확장 합니다 **리소스 파일** 폴더.manifest 파일을 두 번 클릭 합니다.

- 다른 편집기에서 **솔루션 탐색기**.manifest 파일을 마우스 오른쪽 단추로 클릭 하 고 선택 **연결 프로그램...**  바로 가기 메뉴에서. 에 **연결** 대화 상자에서 사용 하 고 선택 하려는 편집기를 지정한 **오픈**합니다.

> [!NOTE]
> 모듈별로 매니페스트 리소스를 하나만 사용할 수 있습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 편집기](../windows/resource-editors.md)<br/>
[리소스 파일 작업](../windows/working-with-resource-files.md)<br/>
[메뉴 및 기타 리소스](https://msdn.microsoft.com/library/windows/desktop/ms632583.aspx)<br/>
[컨트롤](../mfc/controls-mfc.md)<br/>