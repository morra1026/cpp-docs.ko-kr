---
title: /TLBID(TypeLib의 리소스 ID 지정)
ms.date: 11/04/2016
f1_keywords:
- /tlbid
- VC.Project.VCLinkerTool.TypeLibraryResourceID
helpviewer_keywords:
- tlb files, specifying resource ID
- -TLBID linker option
- .tlb files, specifying resource ID
- /TLBID linker option
- TLBID linker option
- type libraries, specifying resource ID
ms.assetid: 434b28a2-4656-4d52-ac82-8b18bf486fb2
ms.openlocfilehash: 1a86c753aa94302e7f4d26c53fee2f63175d33c7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50519290"
---
# <a name="tlbid-specify-resource-id-for-typelib"></a>/TLBID(TypeLib의 리소스 ID 지정)

```
/TLBID:id
```

## <a name="arguments"></a>인수

*ID*<br/>
링커에서 만든 형식 라이브러리에 대 한 사용자 지정 값입니다. 기본 리소스 id 1 대신 사용 됩니다.

## <a name="remarks"></a>설명

특성을 사용 하는 프로그램을 컴파일할 때 링커에서 형식 라이브러리를 만듭니다. 1의 리소스 ID를 형식 라이브러리에 할당 합니다.

기존 리소스 중 하나를 사용 하 여이 리소스 ID 충돌, /TLBID를 사용 하 여 다른 ID를 지정할 수 있습니다. 에 전달할 수 있는 값의 범위 `id` 는 1부터 65535 까지입니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **포함 IDL** 속성 페이지.

1. 수정 된 **TypeLib 리소스 ID** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

1. <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.TypeLibraryResourceID%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)