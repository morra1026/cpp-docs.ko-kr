---
title: /WINMDKEYFILE(winmd 키 파일 지정)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.WINMDKeyFile
ms.assetid: 65d88fdc-fff9-49ea-8cfc-b2f408741734
ms.openlocfilehash: 33481033267d6470db38f0b64e76f5be7b4cbe2f
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57425408"
---
# <a name="winmdkeyfile-specify-winmd-key-file"></a>/WINMDKEYFILE(winmd 키 파일 지정)

Windows 런타임 메타데이터(.winmd) 파일을 서명하기 위한 키 또는 키 쌍을 지정합니다.

```
/WINMDKEYFILE:filename
```

## <a name="remarks"></a>설명

와 유사 합니다 [/KEYFILE](../../build/reference/keyfile-specify-key-or-key-pair-to-sign-an-assembly.md) .winmd 파일에 적용 되는 링커 옵션입니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **링커** 폴더입니다.

1. 선택 된 **Windows 메타 데이터** 속성 페이지.

1. 에 **Windows 메타 데이터 키 파일** 상자 파일 위치를 입력 합니다.

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
