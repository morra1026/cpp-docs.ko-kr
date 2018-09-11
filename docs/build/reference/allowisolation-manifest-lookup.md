---
title: -ALLOWISOLATION (매니페스트 조회) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /ALLOWISOLATION
- VC.Project.VCLinkerTool.AllowIsolation
dev_langs:
- C++
helpviewer_keywords:
- -ALLOWISOLATION linker option
- /ALLOWISOLATION linker option
ms.assetid: 6d41851e-b3c1-4bdf-beaa-031773089d6f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c9197e67e46932f08a266258c41dab7922af2900
ms.sourcegitcommit: f0c90000125a9497bf61e41624de189a043703c0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44318982"
---
# <a name="allowisolation-manifest-lookup"></a>/ALLOWISOLATION(매니페스트 조회)

매니페스트 조회 동작을 지정합니다.

## <a name="syntax"></a>구문

```
/ALLOWISOLATION[:NO]
```

## <a name="remarks"></a>설명

**/ALLOWISOLATION:NO** 매니페스트가 없는 것 처럼 Dll이 로드 되도록 링커가 설정 하 고는 `IMAGE_DLLCHARACTERISTICS_NO_ISOLATION` 선택적인 헤더의 비트 `DllCharacteristics` 필드입니다.

**/ALLOWISOLATION** 매니페스트 조회 및 로드가 수행 하려면 운영 체제입니다.

**/ALLOWISOLATION** 가 기본값입니다.

실행 파일에 대 한 격리 비활성화 되 면 Windows 로더가 새로 생성된 되는 프로세스에 대 한 응용 프로그램 매니페스트를 찾으려고 시도 하지 않습니다. 실행 파일 또는 배치 된 이름 가진 실행 파일과 동일한 디렉터리에 내부 매니페스트가 경우에 새 프로세스에는 기본 활성화 컨텍스트가 없는 됩니다 <em>실행 파일 이름</em>**. exe.manifest**합니다.

자세한 내용은 [매니페스트 파일 참조](/windows/desktop/SbsCs/manifest-files-reference)합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **구성 속성** > **링커** > **매니페스트 파일** 속성 페이지.

1. 수정 된 **격리 허용** 속성입니다.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
