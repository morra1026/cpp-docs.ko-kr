---
title: 링커 명령줄 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- linker [C++], syntax
- linker command line [C++]
- LINK tool [C++], command-line syntax
ms.assetid: e2a31e17-77bd-4e74-9305-75b105b26539
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5f1e891d91b96c5f29fb01dae5b1b8b9d731cdf3
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45718345"
---
# <a name="linker-command-line-syntax"></a>링커 명령줄 구문

링크를 실행 합니다. EXE, 다음 명령 구문을 사용 합니다.

```
LINK arguments
```

`arguments` 옵션과 파일 이름이 포함 되며 순서에 관계 없이 지정할 수 있습니다. 처리 된 가장 먼저 다음 파일은 옵션입니다. 인수를 구분 하려면 하나 이상의 공백이 나 탭을 사용 합니다.

> [!NOTE]
>  Visual Studio 명령 프롬프트 에서만에서이 도구를 시작할 수 있습니다. 시스템 명령 프롬프트 또는 파일 탐색기에서는 시작할 수 없습니다.

명령줄에서 옵션 구성 옵션 지정자를 대시 (-) 또는 슬래시 (/) 옵션의 이름이 차례로 나옵니다. 옵션 이름은 간략 한 형태로 사용할 수 없습니다. 콜론 (:) 뒤에 지정 된 인수를 사용 하는 몇 가지 옵션입니다. 공백 또는 탭 수를 옵션 사양 내에서 제외 하 고 /COMMENT 옵션에서 따옴표 붙은 문자열 내에서. 10 진수 또는 C 언어 표기법으로 숫자 인수를 지정 합니다. 옵션 이름 및 해당 키워드 또는 filename 인수는 대 소문자를 구분 하지 않지만 인수로 식별자가 대/소문자 구분 합니다.

파일을 링커에 전달할 링크 명령 후 명령줄에서 파일 이름을 지정 합니다. 에 파일 이름을 사용 하 여 절대 또는 상대 경로 지정할 수 있습니다 및 파일 이름에 와일드 카드를 사용할 수 있습니다. 점 (.) 및 파일 이름 확장명을 생략 하면 링크는.obj 파일을 찾기 위해 가정 합니다. 링크 또는 사용 하지 파일 이름 확장명의 부족을 통해 파일의 콘텐츠에 대 한 가정 검사 하 여 파일의 형식을 결정 하 고 적절 하 게 처리 합니다.

link.exe 성공 (오류 없음)에 대 한 0을 반환합니다.  링커, 링크를 중지 하는 오류 번호를 반환 합니다.  예를 들어 링커가 LNK1104를 생성할 경우에 링커가 1104를 반환 합니다.  따라서 링커에서 오류로 반환 되는 최저 오류 번호는 1000 개입니다.  반환 값이 128 나타내는 운영 체제 또는.config 파일에 구성 문제가 로더가는 link.exe 또는 c2.dll을 로드 되지 않았습니다.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)