---
title: -INTEGRITYCHECK (시그니처 확인 필요) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
ms.assetid: 9e738825-2c98-40cd-8ad2-5d0d9c14893e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 31df513a40b60fcb57c48f0d20e124fc77888d99
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45703128"
---
# <a name="integritycheck-require-signature-check"></a>/INTEGRITYCHECK(시그니처 확인 필요)

로드 시 이진 이미지의 디지털 서명을 확인 해야 합니다는 나타냅니다.

```
/INTEGRITYCHECK[:NO]
```

## <a name="remarks"></a>설명

기본적으로 **/INTEGRITYCHECK** 꺼져 있습니다.

합니다 **/INTEGRITYCHECK** 옵션 집합-DLL 파일 또는 실행 파일의 PE 헤더에서-Windows에서 이미지를 로드 하려면 디지털 서명을 확인 하는 메모리 관리자에 대 한 플래그입니다. 이 옵션은 특정 Windows 기능으로 로드 되는 커널 모드 코드를 구현 하는 32 비트 및 64 비트 Dll에 대 한 설정 해야 하며 Windows Vista, Windows 7, Windows 8, Windows Server 2008 및 Windows Server 2012에서 모든 장치 드라이버에 대 한 것이 좋습니다. Windows Vista 이전의 Windows 버전은이 플래그를 무시 합니다. 자세한 내용은 [강제 무결성 서명의 PE (이식 가능) 파일](http://social.technet.microsoft.com/wiki/contents/articles/255.forced-integrity-signing-of-portable-executable-pe-files.aspx)합니다.

### <a name="to-set-this-linker-option-in-visual-studio"></a>Visual Studio에서 이 링커 옵션을 설정하려면

1. 프로젝트 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **구성 속성** 노드를 확장합니다.

1. 확장 된 **링커** 노드.

1. 선택 된 **명령줄** 속성 페이지.

1. **추가 옵션**를 입력 `/INTEGRITYCHECK` 또는 `/INTEGRITYCHECK:NO`합니다.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)<br/>
[무결성 서명의 PE (이식 가능) 파일을 강제로](http://social.technet.microsoft.com/wiki/contents/articles/255.forced-integrity-signing-of-portable-executable-pe-files.aspx)
[커널 모드 코드 서명 연습](https://msdn.microsoft.com/windows/hardware/gg487328.aspx)<br/>
[Windows 7 및 Windows Server 2008의 AppInit Dll](https://msdn.microsoft.com/windows/hardware/gg463040.aspx)