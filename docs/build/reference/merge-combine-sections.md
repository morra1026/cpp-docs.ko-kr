---
title: /병합(섹션 결합)
ms.date: 11/04/2016
f1_keywords:
- /merge
- VC.Project.VCLinkerTool.MergeSections
helpviewer_keywords:
- sections, combining
- /MERGE linker option
- sections, naming
- sections
- -MERGE linker option
- MERGE linker option
ms.assetid: 10fb20c2-0b3f-4c8d-98a8-f69aedf03d52
ms.openlocfilehash: d9e029bf38beab83e7823a65376a70278c82d34c
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57414722"
---
# <a name="merge-combine-sections"></a>/병합(섹션 결합)

```
/MERGE:from=to
```

## <a name="remarks"></a>설명

/MERGE 옵션 첫 번째 섹션을 결합 (*에서*) 두 번째 섹션을 사용 하 여 (*하*), 결과 섹션 명명 *를*합니다. 예를 들어, `/merge:.rdata=.text`을 입력합니다.

두 번째 섹션 존재 하지 않는 링크 섹션 이름을 바꿉니다 *에서* 으로 *에*입니다.

/MERGE 옵션 Vxd 만들고 컴파일러에서 생성 된 섹션 이름을 재정의에 유용 합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **고급** 속성 페이지.

1. 수정 된 **병합 섹션** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

1. <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.MergeSections%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
