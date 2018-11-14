---
title: /DEFAULTLIB(기본 라이브러리 지정)
ms.date: 05/29/2018
f1_keywords:
- VC.Project.VCLinkerTool.DefaultLibraries
- /defaultlib
helpviewer_keywords:
- -DEFAULTLIB linker option
- DEFAULTLIB linker option
- /DEFAULTLIB linker option
- libraries, adding to list of
ms.assetid: 6af7ff49-c170-4a13-97e2-2b9ae2de20c9
ms.openlocfilehash: 59a4b48e412cee6b2a90608747aa6fb3e1b79ca7
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326388"
---
# <a name="defaultlib-specify-default-library"></a>/DEFAULTLIB(기본 라이브러리 지정)

외부 참조를 확인 하기 위해 검색할 기본 라이브러리를 지정 합니다.

## <a name="syntax"></a>구문

> **/DEFAULTLIB**:_라이브러리_

### <a name="arguments"></a>인수

*라이브러리*<br/>
외부 참조를 확인할 때 검색할 라이브러리의 이름입니다.

## <a name="remarks"></a>설명

합니다 **/DEFAULTLIB** 옵션에는 추가 *라이브러리* 링크 참조를 확인할 때 검색 하는 라이브러리 목록에 있습니다. 지정 된 라이브러리 **/DEFAULTLIB** .obj 파일에 지정 된 기본 라이브러리 전과 명령줄에서 명시적으로 지정 하는 라이브러리 후 검색 됩니다.

인수 없이 사용 하는 경우는 [/NODEFAULTLIB (모든 기본 라이브러리 무시)](../../build/reference/nodefaultlib-ignore-libraries.md) 옵션을 모두 무시 **/DEFAULTLIB**:*라이브러리* 옵션입니다. 합니다 **/NODEFAULTLIB**:*라이브러리* 재정의 옵션 **/DEFAULTLIB**:*라이브러리* 때 동일한 *라이브러리*둘 다에 이름을 지정 합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **구성 속성** > **링커** > **명령줄** 속성 페이지.

1. **추가 옵션**를 입력 한 **/DEFAULTLIB**:*라이브러리* 검색할 각 라이브러리에 대 한 옵션입니다. 선택할 **확인** 변경 내용을 저장 합니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

- [링커 옵션 설정](../../build/reference/setting-linker-options.md)
- [링커 옵션](../../build/reference/linker-options.md)
