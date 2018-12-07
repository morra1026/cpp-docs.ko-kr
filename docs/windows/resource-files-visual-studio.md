---
title: 리소스 파일(C++)
ms.date: 11/04/2016
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
ms.assetid: 4d2b6fcc-07cf-4289-be87-83a60f69533c
ms.openlocfilehash: 9ad36f19185bc5b3430e7644ef55164d3cb0839a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50461700"
---
# <a name="resource-files-c"></a>리소스 파일(C++)

> [!NOTE]
> 이 자료는 Windows 데스크톱 응용 프로그램에 적용됩니다. 유니버설 Windows 플랫폼 앱의 리소스에 대한 자세한 내용은 [앱 리소스 정의](/windows/uwp/app-resources/)를 참조하세요.
>
> 관리되는 프로젝트에 리소스를 추가하는 방법에 대한 정보는 *.NET 프레임워크 개발자 가이드*의 [데스크톱 앱의 리소스](/dotnet/framework/resources/index)를 참조하세요. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 액세스, 정적 리소스 표시 및 속성에 리소스 문자열을 할당하는 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 리소스 지역화에 대한 내용은 [Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)를 참조하세요.
>
> .NET 프로그래밍 언어의 프로젝트는 리소스 스크립트 파일을 사용하지 않으므로 **솔루션 탐색기**에서 리소스를 열어야 합니다. 관리되는 프로젝트에서 리소스 파일로 작업하려면 [이미지 편집기](../windows/image-editor-for-icons.md) 및 [바이너리 편집기](binary-editor.md)를 사용할 수 있습니다. 편집하고자 하는 관리되는 모든 리소스는 연결된 리소스여야 합니다. Visual Studio 리소스 편집기에서는 포함된 리소스를 편집할 수 없습니다.

"리소스 파일"이라는 용어는 다음을 포함한 여러 파일 형식을 나타낼 수 있습니다.

- 프로그램의 리소스 스크립트(.rc) 파일

- 리소스 템플릿(.rct) 파일

- .rc 파일에서 참조되는 비트맵, 아이콘 또는 커서 파일과 같이 독립 실행형 파일로 존재하는 개별 리소스

- .rc 파일에서 참조되며 개발 환경에서 생성된 헤더 파일(예: Resource.h)

또한 .exe, .dll 및 .res 파일과 같은 [다른 파일 형식](../windows/editable-file-types-for-resources.md)의 리소스도 찾아볼 수 있습니다. 프로젝트 내의 리소스나 현재 프로젝트에 포함되지 않은 리소스 및 리소스 파일에 대한 작업도 할 수 있습니다. 또한 Visual Studio 개발 환경에서 생성되지 않은 리소스 파일에 대한 작업도 할 수 있습니다. 예를 들어 다음 작업을 할 수 있습니다.

- 중첩되어 조건부로 포함된 리소스 파일에 대한 작업

- 기존 리소스 업데이트 또는 Visual C++ 형식으로 변환

- 현재 리소스 파일에서 그래픽 리소스 가져오기 또는 내보내기

- 개발 환경에서 수정할 수 없는 공유 또는 읽기 전용 식별자(기호) 포함

- 여러 프로젝트 간에 공유되는 리소스와 같이 현재 프로젝트에서 편집할 필요가 없거나 편집하지 않으려는 실행 파일(.exe)의 리소스 포함

- 개발 환경에서 지원하지 않는 리소스 형식 포함

이 섹션에서는 다음을 설명합니다.

- [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)

- [새 리소스 만들기](../windows/how-to-create-a-resource.md)

- [리소스 스크립트 파일의 리소스 보기](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)

- [리소스 스크립트 파일을 텍스트 형식으로 열기](../windows/how-to-open-a-resource-script-file-in-text-format.md)

- [컴파일 시간에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)

- [리소스 복사](../windows/how-to-copy-resources.md)

- [리소스 템플릿(.rct) 사용](../windows/how-to-use-resource-templates.md)

- [리소스 가져오기 및 내보내기](../windows/how-to-import-and-export-resources.md)

- [편집할 수 있는 리소스 파일 형식](../windows/editable-file-types-for-resources.md)

- [리소스 편집의 영향을 받는 파일](../windows/files-affected-by-resource-editing.md)

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[리소스 편집기](../windows/resource-editors.md)<br/>
[리소스 파일 작업](../windows/working-with-resource-files.md)<br/>
[메뉴 및 기타 리소스](https://msdn.microsoft.com/library/windows/desktop/ms632583.aspx)
