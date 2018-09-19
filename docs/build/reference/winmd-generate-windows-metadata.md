---
title: -WINMD (Windows 메타 데이터 생성) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.GenerateWindowsMetadata
dev_langs:
- C++
ms.assetid: bcfb4901-411e-4c9e-9f78-23028b6e5fcc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 25b8b34e55fc0814653f4c44be50e545633be373
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45705732"
---
# <a name="winmd-generate-windows-metadata"></a>/WINMD(Windows 메타데이터 생성)

Windows 런타임 메타데이터(.winmd) 파일을 생성할 수 있게 해줍니다.

```
/WINMD[:{NO|ONLY}]
```

## <a name="remarks"></a>설명

**/ WINMD**<br/>
유니버설 Windows 플랫폼 앱에 대 한 기본 설정입니다. 링커가 바이너리 실행 파일 및 .winmd 메타데이터 파일을 모두 생성합니다.

**/WINMD:NO**<br/>
링커가 바이너리 실행 파일만 생성하고 .winmd 파일은 생성하지 않습니다.

**/ WINMD:만**<br/>
링커가 .winmd 파일만 생성하고 바이너리 실행 파일은 생성하지 않습니다.

기본적으로 출력 파일 이름의 형식은 `binaryname`.winmd입니다. 다른 파일 이름을 지정 하려면 사용 합니다 [/WINMDFILE](../../build/reference/winmdfile-specify-winmd-file.md) 옵션입니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **링커** 폴더입니다.

1. 선택 된 **Windows 메타 데이터** 속성 페이지.

1. 에 **Windows 메타 데이터 생성** 드롭다운 목록 상자에서 원하는 옵션을 선택 합니다.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)