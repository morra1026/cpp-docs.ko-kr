---
title: -RELEASE (체크섬 설정) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /release
- VC.Project.VCLinkerTool.SetChecksum
dev_langs:
- C++
helpviewer_keywords:
- -RELEASE linker option
- /RELEASE linker option
- checksum setting
- RELEASE linker option
ms.assetid: 93bcadf4-29ac-4824-914b-6997e3751d22
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 69439400ec58e2d41ef0359237b30ea09c5fd170
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45710075"
---
# <a name="release-set-the-checksum"></a>/RELEASE(체크섬 설정)

```
/RELEASE
```

## <a name="remarks"></a>설명

/RELEASE 옵션은.exe 파일의 헤더에 체크섬을 설정 합니다.

운영 체제 장치 드라이버에 대 한 체크섬이 필요 합니다. 이후 운영 체제와 호환성을 위해 장치 드라이버의 릴리스 버전에 대 한 체크섬을 설정 합니다.

/RELEASE 옵션은 기본적으로 설정 됩니다 때 합니다 [/SUBSYSTEM:NATIVE](../../build/reference/subsystem-specify-subsystem.md) 옵션을 지정 합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **고급** 속성 페이지.

1. 수정 된 **체크섬 설정** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.SetChecksum%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)