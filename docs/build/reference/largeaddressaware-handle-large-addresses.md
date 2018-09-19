---
title: -LARGEADDRESSAWARE (큰 주소 처리) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.LargeAddressAware
- /largeaddressaware
dev_langs:
- C++
helpviewer_keywords:
- LARGEADDRESSAWARE linker option
- -LARGEADDRESSAWARE linker option
- /LARGEADDRESSAWARE linker option
ms.assetid: a29756c8-e893-47a9-9750-1f0d25359385
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0a68b18f912d7e6ca0f0f642c85e8439be0e5b67
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45726331"
---
# <a name="largeaddressaware-handle-large-addresses"></a>/LARGEADDRESSAWARE(큰 주소 처리)

```
/LARGEADDRESSAWARE[:NO]
```

## <a name="remarks"></a>설명

/LARGEADDRESSAWARE 옵션을 링커에 지시할 수 응용 프로그램에서 2gb 보다 큰 주소를 처리할 수 있도록 합니다. 64 비트 컴파일러에서이 옵션은 기본적으로 사용 됩니다. 32 비트 컴파일러에 /largeaddressaware: no /LARGEADDRESSAWARE 링커 줄에서 그렇지 않은 경우 지정 하지 않은 경우 사용 됩니다.

/LARGEADDRESSAWARE, DUMPBIN 사용 하 여 응용 프로그램 연결 된 경우 [/HEADERS](../../build/reference/headers.md) 그 결과 정보가 표시 됩니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **시스템** 속성 페이지.

1. 수정 된 **큰 주소 사용** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.LargeAddressAware%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)