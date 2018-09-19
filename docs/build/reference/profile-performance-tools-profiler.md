---
title: -PROFILE (성능 도구 Profiler) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.Profile
dev_langs:
- C++
helpviewer_keywords:
- -PROFILE linker option
- /PROFILE linker option
ms.assetid: e676baa1-5063-47a3-a357-ba0d1f0d1699
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 859ea4091502fa6c339a809a5b9e439c91462bd7
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45707768"
---
# <a name="profile-performance-tools-profiler"></a>/PROFILE(성능 도구 프로파일러)

성능 도구 프로파일러와 함께 사용할 수 있는 출력 파일을 생성합니다.

## <a name="syntax"></a>구문

```
/PROFILE
```

## <a name="remarks"></a>설명

/ 프로필 의미 링커 옵션은 다음과 같습니다.

- [/OPT: REF](../../build/reference/opt-optimizations.md)

- /OPT: NOICF

- [/INCREMENTAL: NO](../../build/reference/incremental-link-incrementally.md)

- [/FIXED: NO](../../build/reference/fixed-fixed-base-address.md)

/ 프로필 사용 하면 링커가 프로그램 이미지에서 재배치 섹션 생성 합니다.  재배치 섹션 프로파일러를 프로필 데이터를 가져올 프로그램 이미지를 변환할 수 있습니다.

**/ 프로필** 만 (팀 개발) 엔터프라이즈 버전 에서만에서 제공 됩니다.  PREfast에 대 한 자세한 내용은 참조 하세요. [C/c + + 개요에 대 한 코드 분석](/visualstudio/code-quality/code-analysis-for-c-cpp-overview)합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **구성 속성** 노드를 확장합니다.

1. 확장 된 **링커** 노드.

1. 선택 된 **고급** 속성 페이지.

1. 수정 된 **프로필** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

1. <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.Profile%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)