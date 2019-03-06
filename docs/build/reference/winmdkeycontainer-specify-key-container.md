---
title: /WINMDKEYCONTAINER(키 컨테이너 지정)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.WINMDKEYCONTAINER
ms.assetid: c2fc44dc-7cb5-42b9-897f-1b124928f2f7
ms.openlocfilehash: 5424b928f80bf73aedb731f835b72d20bfd0c4a2
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57416594"
---
# <a name="winmdkeycontainer-specify-key-container"></a>/WINMDKEYCONTAINER(키 컨테이너 지정)

Windows 메타데이터(.winmd) 파일을 서명하기 위한 키 컨테이너를 지정합니다.

```
/WINMDKEYCONTAINER:name
```

## <a name="remarks"></a>설명

와 유사 합니다 [/KEYCONTAINER](../../build/reference/keycontainer-specify-a-key-container-to-sign-an-assembly.md) (.winmd) 파일에 적용 되는 링커 옵션입니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **링커** 폴더입니다.

1. 선택 된 **Windows 메타 데이터** 속성 페이지.

1. 에 **Windows 메타 데이터 키 컨테이너** 상자 위치를 입력 합니다.

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
