---
title: C/c + + 빌드 참조 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- compiling source code [C++], additional information
- cl.exe compiler [C++], building programs
- linker [C++], building reference
- builds [C++], additional information
ms.assetid: 100b4ccf-572c-4d1f-970c-fa0bc0cc0d2d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 116ddca6ed9f5e0b3ea02652958931f88cc8fc13
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45703224"
---
# <a name="cc-building-reference"></a>C/C++ 빌드 참조

Visual c + +는 C/c + + 프로그램을 구축 하는 두 가지를 제공 합니다. (가장 쉽고 일반적인) 하는 방법은 [Visual c + + 개발 환경 내에서 빌드](../../ide/building-cpp-projects-in-visual-studio.md)합니다. 다른 방법은 [명령줄 도구를 사용 하 여 명령 프롬프트에서 빌드](../../build/building-on-the-command-line.md)합니다. 두 경우 모두 Visual c + + 소스 편집기 또는 선택한 타사 편집기를 사용 하 여 원본 파일을 만들 수 있습니다.

프로그램이.vcxproj 파일 보다는 메이크파일의 사용 하는 경우 빌드할 수 있습니다이 개발 환경에는 [외부 프로젝트](../../ide/building-external-projects.md)합니다.

## <a name="in-this-section"></a>섹션 내용

[C/c + + 프로그램 컴파일](../../build/reference/compiling-a-c-cpp-program.md) 기계어 코드, 링커 지시문, 섹션, 외부 참조 이름과 함수/데이터를 포함 하는 개체 파일을 만드는 컴파일러에 설명 합니다.

[연결](../../build/reference/linking.md) 설명 정적으로 연결 된 라이브러리 및 컴파일러에 의해 생성 된 개체 파일에서 코드를 결합 하는 링커 이름 참조를 확인 하 고 실행 파일을 만듭니다.

[릴리스 빌드](../../build/reference/release-builds.md) 릴리스 빌드를 디버그 빌드에서 변경 하려는 이유와 시기에 대 한 정보를 제공 하 고도 디버그에서 릴리스 빌드를로 변경할 때 발생할 수 있습니다 문제 중 일부를 설명 합니다.

[코드 최적화](../../build/reference/optimizing-your-code.md) 코드를 최적화 하기 위한 메커니즘을 설명 하는 항목에 대 한 링크를 제공 합니다.

[C/c + + Build Tools](../../build/reference/c-cpp-build-tools.md) 보거나 빌드 출력을 조작 하기 위한 다음과 같은 명령줄 도구를 제공 합니다.

[C/c + + 빌드 오류](../../error-messages/compiler-errors-1/c-cpp-build-errors.md) 내용의 테이블의 빌드 오류 섹션을 소개 합니다.

## <a name="related-sections"></a>관련 단원

[C/c + + 전처리기 참조](../../preprocessor/c-cpp-preprocessor-reference.md) 매크로, 연산자 및 지시문을 변환 하 여 컴파일러에 대 한 소스 파일을 준비 하는 전처리기에 설명 합니다.

[사용자 지정 빌드 단계 및 빌드 이벤트 이해](../../ide/understanding-custom-build-steps-and-build-events.md) 빌드 프로세스를 사용자 지정에 대해 설명 합니다.

[C/c + + 프로그램 빌드](../../build/building-c-cpp-programs.md) 명령줄 또는 Visual Studio 통합된 개발 환경에서 프로그램 빌드를 설명 하는 항목에 대 한 링크를 제공 합니다.

[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md) 개발 환경에서 또는 명령줄에서 컴파일러 옵션 설정에 설명 합니다.

[컴파일러 옵션](../../build/reference/compiler-options.md) 컴파일러 옵션을 사용 하 여 설명 하는 항목에 대 한 링크를 제공 합니다.

[링커 옵션 설정](../../build/reference/setting-linker-options.md) 통합된 개발 환경 외부 또는 내부 링커 옵션 설정에 설명 합니다.

[링커 옵션](../../build/reference/linker-options.md) 링커 옵션을 사용 하 여 설명 하는 항목에 대 한 링크를 제공 합니다.

[BSCMAKE 참조](../../build/reference/bscmake-reference.md) Microsoft 찾아보기 Information Maintenance Utility (BSCMAKE에 설명 합니다. EXE)에 찾아보기 정보 파일 (.bsc)에서 빌드합니다.sbr 파일 컴파일 중에 생성 합니다.

[LIB 참조](../../build/reference/lib-reference.md) 만들고 COFF 공용 개체 파일 형식 () 개체 파일의 라이브러리를 관리 하는 Microsoft 라이브러리 관리자 (LIB.exe)에 대해 설명 합니다.

[EDITBIN 참조](../../build/reference/editbin-reference.md) Microsoft COFF Binary 파일 편집기 (EDITBIN 합니다. 개체 파일 형식 COFF (공용) 이진 파일을 수정 하는 EXE).

[DUMPBIN 참조](../../build/reference/dumpbin-reference.md) Microsoft COFF Binary File Dumper (DUMPBIN에 설명 합니다. Exe)에 개체 파일 형식 COFF (공용) 이진 파일에 대 한 정보입니다.

[NMAKE 참조](../../build/nmake-reference.md) Microsoft Program Maintenance Utility (NMAKE에 설명 합니다. 프로젝트를 빌드하는 도구는 EXE)을 설명 파일에 포함 된 명령을 기반으로 합니다.