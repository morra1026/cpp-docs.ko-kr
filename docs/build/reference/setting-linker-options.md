---
title: 링커 옵션 설정
ms.date: 11/04/2016
helpviewer_keywords:
- files [C++], LINK
- input files [C++], linker
- linker [C++], ways to set options
- linker [C++], switches
- input files [C++]
- object/library modules
ms.assetid: e08fb487-0f2e-4f24-87db-232dbc8bd2e2
ms.openlocfilehash: 5b885ad5c86bc59029fc6a3a60ccee385703ab2d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50508942"
---
# <a name="setting-linker-options"></a>링커 옵션 설정

링커 옵션은 개발 환경 내부 또는 외부에서 설정할 수 있습니다. 각 링커 옵션 항목에서는 개발 환경에서 해당 링커 옵션을 설정하는 방법에 대해 설명합니다. 전체 목록은 [링커 옵션](../../build/reference/linker-options.md)을 참조하십시오.

개발 환경 외부에서 LINK를 실행하면 다음 방법으로 입력을 지정할 수 있습니다.

- [명령줄](../../build/reference/linker-command-line-syntax.md) 사용

- [명령 파일](../../build/reference/link-command-files.md) 사용

- [환경 변수](../../build/reference/link-environment-variables.md) 사용

LINK를 실행하면 LINK 환경 변수에 지정된 옵션이 먼저 처리된 다음 명령줄과 명령 파일에 지정된 옵션이 순서대로 처리됩니다. 서로 다른 인수를 사용하여 동일한 옵션을 반복하는 경우에는 마지막으로 처리된 옵션이 가장 우선합니다.

옵션은 전체 빌드에 적용되지만 특정 입력 파일에는 옵션이 적용되지 않을 수도 있습니다.

## <a name="see-also"></a>참고 항목

[C/C++ 빌드 참조](../../build/reference/c-cpp-building-reference.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
