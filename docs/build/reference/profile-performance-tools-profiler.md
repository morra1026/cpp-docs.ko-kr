---
title: /PROFILE(성능 도구 프로파일러)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.Profile
helpviewer_keywords:
- -PROFILE linker option
- /PROFILE linker option
ms.assetid: e676baa1-5063-47a3-a357-ba0d1f0d1699
ms.openlocfilehash: a0fda47497ffc247dd9678ece7aac76291aed1ff
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57419155"
---
# <a name="profile-performance-tools-profiler"></a>/PROFILE(성능 도구 프로파일러)

성능 도구 프로파일러와 함께 사용할 수 있는 출력 파일을 생성합니다.

## <a name="syntax"></a>구문

```
/PROFILE
```

## <a name="remarks"></a>설명

/ 프로필 의미 링커 옵션은 다음과 같습니다.

- [/OPT:REF](../../build/reference/opt-optimizations.md)

- /OPT: NOICF

- [/INCREMENTAL:NO](../../build/reference/incremental-link-incrementally.md)

- [/FIXED:NO](../../build/reference/fixed-fixed-base-address.md)

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

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
