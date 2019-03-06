---
title: /IGNOREIDL (Don&#39;t 프로세스 특성을 MIDL로)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.IgnoreEmbeddedIDL
- /ignoreidl
helpviewer_keywords:
- IGNOREIDL linker option
- -IGNOREIDL linker option
- /IGNOREIDL linker option
ms.assetid: 29514098-6a1c-4317-af2f-1dc268972780
ms.openlocfilehash: 1a78f99f61bbeff9c5d617fce374925d0541aafd
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57423159"
---
# <a name="ignoreidl-don39t-process-attributes-into-midl"></a>/IGNOREIDL (Don&#39;t 프로세스 특성을 MIDL로)

```
/IGNOREIDL
```

## <a name="remarks"></a>설명

/IGNOREIDL 옵션 지정 [IDL 특성](../../windows/idl-attributes.md) 원본.idl 파일 코드 처리 되지 않도록 합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **포함 IDL** 속성 페이지.

1. 수정 된 **포함 IDL 무시** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.IgnoreEmbeddedIDL%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)<br/>
[/IDLOUT(MIDL 출력 파일 이름 지정)](../../build/reference/idlout-name-midl-output-files.md)<br/>
[/TLBOUT(.TLB 파일 이름 지정)](../../build/reference/tlbout-name-dot-tlb-file.md)<br/>
[/MIDL(MIDL 명령줄 옵션 지정)](../../build/reference/midl-specify-midl-command-line-options.md)<br/>
[특성을 사용하는 프로그램 빌드](../../windows/building-an-attributed-program.md)
