---
title: /NOLOGO(시작 배너 표시 안 함)(링커)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.SuppressStartupBanner
- /nologo
helpviewer_keywords:
- suppress startup banner linker option
- -NOLOGO linker option
- /NOLOGO linker option
- copyright message
- version numbers, preventing linker display
- banners, suppressing startup
- NOLOGO linker option
ms.assetid: 3b20dddd-eca6-4545-a331-9f70bf720197
ms.openlocfilehash: d246da2e10f7c16f7c194962841e2e44d1fd1758
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50515546"
---
# <a name="nologo-suppress-startup-banner-linker"></a>/NOLOGO(시작 배너 표시 안 함)(링커)

```
/NOLOGO
```

## <a name="remarks"></a>설명

/NOLOGO 옵션 저작권 메시지 및 버전 번호를 표시를 하지 않습니다.

이 옵션에는 명령 파일의 에코 하지 않습니다. 자세한 내용은 참조 하세요 [LINK 명령 파일](../../build/reference/link-command-files.md)합니다.

기본적으로이 정보는 출력 창에 링커를 통해 전송 됩니다. 명령줄에서 클래스는 표준 출력으로 전송 되 고 파일로 리디렉션할 수 있습니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 이 옵션은 명령줄에서만 사용 해야 합니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

1. 이 링커 옵션을 프로그래밍 방식으로 변경할 수 없습니다.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)