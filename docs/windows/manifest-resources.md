---
title: 매니페스트 리소스 (c + +)
ms.date: 11/04/2016
helpviewer_keywords:
- manifest resources [C++]
- resources [C++], manifest
ms.assetid: 8615334c-22a0-44c0-93e0-5924528c9917
ms.openlocfilehash: 081fd12a86c31973c7856ca7b9f3fcb129e2eb81
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50578284"
---
# <a name="manifest-resources-c"></a>매니페스트 리소스 (c + +)

C + + 데스크톱 프로젝트에서 매니페스트 리소스는 응용 프로그램에서 사용 하는 종속성을 설명 하는 XML 파일입니다. 예를 들어 Visual Studio의 MFC 마법사에서 생성되는 매니페스트 파일은 응용 프로그램이 Windows 공용 컨트롤 DLL 버전 5.0 또는 6.0 중 어느 것을 사용해야 하는지 정의합니다.

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

Windows XP 또는 Windows Vista 응용 프로그램의 경우, 매니페스트 리소스는 응용 프로그램이 최신 버전(위에 나온 대로 v6.0)의 Windows 공용 컨트롤을 사용하도록 지정할 뿐만 아니라 [Syslink 컨트롤](/windows/desktop/Controls/syslink-overview)도 지원합니다.

버전을 보려면 매니페스트 리소스에 포함 된 정보를 입력을 XML 뷰어 또는 Visual Studio 텍스트 편집기에서 파일을 열 수 있습니다. 자세한 내용은 [Visual Studio 텍스트 편집기에서 매니페스트 리소스 열기](../windows/how-to-open-a-manifest-resource.md)를 참조하세요.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다.

## <a name="limitations"></a>제한 사항

모듈별로 매니페스트 리소스를 하나만 사용할 수 있습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[컨트롤](../mfc/controls-mfc.md)<br/>
[리소스 파일 작업](../windows/working-with-resource-files.md)