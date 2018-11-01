---
title: 컴파일러 옵션
ms.date: 01/29/2018
helpviewer_keywords:
- cl.exe compiler
- x86 Visual C++ compiler
- ARM Visual C++ compiler
- compiler options, C++
- x64 Visual C++ compiler
ms.assetid: ed3376c8-bef4-4c9a-80e9-3b5da232644c
ms.openlocfilehash: 8b887b2b9da6f38cdc1cf7287a69bbad8e88b989
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50583887"
---
# <a name="compiler-options"></a>컴파일러 옵션

cl.exe는 Microsoft Visual c + + (MSVC) C 및 c + + 컴파일러 및 링커를 제어 하는 도구입니다. cl.exe는 Microsoft Visual Studio에 대 한 Windows를 지 원하는 운영 체제 에서만 실행할 수 있습니다.

> [!NOTE]
> Visual Studio 개발자 명령 프롬프트 에서만에서이 도구를 시작할 수 있습니다. 시스템 명령 프롬프트 또는 파일 탐색기에서는 시작할 수 없습니다. 자세한 내용은 [명령줄에서 빌드 C/c + + 코드](../building-on-the-command-line.md)합니다.

컴파일러는 COFF 공용 개체 파일 형식 () 개체 (.obj) 파일을 생성합니다. 링커는 실행 파일 (.exe) 또는 동적 연결 라이브러리 (Dll)를 생성 합니다.

모든 컴파일러 옵션은 대/소문자 구분를 참고 합니다. 두 슬래시를 사용할 수 있습니다 (`/`) 또는 대시 (`-`) 컴파일러 옵션을 지정 합니다.

연결 하지 않고 컴파일하면를 사용 합니다 [/c](../../build/reference/c-compile-without-linking.md) 옵션입니다.

## <a name="find-a-compiler-option"></a>컴파일러 옵션 찾기

특정 컴파일러 옵션을 보려면, 다음 목록 중 하나를 참조 하세요.

- [컴파일러 옵션 사전순 목록](../../build/reference/compiler-options-listed-alphabetically.md)

- [컴파일러 옵션 범주별 목록](../../build/reference/compiler-options-listed-by-category.md)

## <a name="specify-compiler-options"></a>컴파일러 옵션을 지정 합니다.

각 컴파일러 옵션에 대 한 설명 하는 방법을 개발 환경에서 설정할 수 있습니다. 개발 환경 밖에 서 옵션을 지정 하는 내용은 다음을 참조 하세요.

- [컴파일러 명령줄 구문](../../build/reference/compiler-command-line-syntax.md)

- [CL 명령 파일](../../build/reference/cl-command-files.md)

- [CL 환경 변수](../../build/reference/cl-environment-variables.md)

## <a name="related-build-tools"></a>관련된 빌드 도구

[링커 옵션](../../build/reference/linker-options.md) 또한 프로그램을 빌드하는 방법에 영향을 줍니다.

## <a name="see-also"></a>참고자료

[C/C++ 빌드 참조](../../build/reference/c-cpp-building-reference.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[컴파일 속도 향상](../../build/reference/fast-compilation.md)<br/>
[CL에서의 링커 호출](../../build/reference/cl-invokes-the-linker.md)
