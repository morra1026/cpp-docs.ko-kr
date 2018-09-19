---
title: 링커 옵션 설정 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- files [C++], LINK
- input files [C++], linker
- linker [C++], ways to set options
- linker [C++], switches
- input files [C++]
- object/library modules
ms.assetid: e08fb487-0f2e-4f24-87db-232dbc8bd2e2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d2fd99732c7f79b3c61ff5b31516b98a478ed4a8
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45713078"
---
# <a name="setting-linker-options"></a>링커 옵션 설정

개발 환경 외부 또는 내부 링커 옵션을 설정할 수 있습니다. 각 링커 옵션에 대 한 항목에서는 개발 환경에서 설정할 수 있습니다 하는 방법을 설명 합니다. 참조 [링커 옵션](../../build/reference/linker-options.md) 목록은 합니다.

개발 환경 외부 링크를 실행 하는 경우에 하나 이상의 방법으로 입력을 지정할 수 있습니다.

- 에 [명령줄](../../build/reference/linker-command-line-syntax.md)

- 사용 하 여 [명령 파일](../../build/reference/link-command-files.md)

- [환경 변수](../../build/reference/link-environment-variables.md)

명령 파일에 명령줄에 지정 된 순서로 옵션 뒤에 링크 환경 변수에 지정 된 링크의 첫 번째 프로세스 옵션입니다. 옵션은 서로 다른 인수를 사용 하 여 반복 되는 경우는 마지막 처리 우선 합니다.

옵션은 전체 빌드;에 적용 옵션 없이 특정 입력된 파일에 적용할 수 있습니다.

## <a name="see-also"></a>참고 항목

[C/C++ 빌드 참조](../../build/reference/c-cpp-building-reference.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)