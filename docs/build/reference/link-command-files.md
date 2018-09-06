---
title: LINK 명령 파일 | Microsoft Docs
ms.custom: ''
ms.date: 09/05/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- link
dev_langs:
- C++
helpviewer_keywords:
- syntax, LINK command files
- command files [C++]
- LINK tool [C++]
- text files, passing arguments to LINK
- LINK tool [C++], command-line syntax
- command files [C++], LINK
ms.assetid: 7154511c-32b9-4e5b-a515-3922fa9de48e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8934758d8aa406ea7b7c959b1fc535cde32195b1
ms.sourcegitcommit: d10a2382832373b900b1780e1190ab104175397f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43894683"
---
# <a name="link-command-files"></a>LINK 명령 파일

명령 파일의 형태로 링크에 명령줄 인수를 전달할 수 있습니다. 링커 명령 파일을 지정 하려면 다음 구문을 사용 합니다.

> **링크 \@**  <em>commandfile</em>

합니다 *commandfile* 텍스트 파일의 이름입니다. 없는 공백 또는 탭 간 허용 되는 at 기호 (**\@**) 및 파일 이름입니다. 기본 확장명이 없습니다. 전체 파일 이름 확장명을 포함 하 여 지정 해야 합니다. 와일드 카드를 사용할 수 없습니다. 파일을 사용 하 여 절대 또는 상대 경로 지정할 수 있습니다. 링크 파일을 검색 하는 환경 변수를 사용 하지 않습니다.

명령 파일의 인수 수 구분 공백이 나 탭 (대로 명령줄에서) 및 줄 바꿈 문자입니다.

명령 파일의 명령줄의 일부나 전부를 지정할 수 있습니다. LINK 명령의 명령 파일을 여러 개 사용할 수 있습니다. 링크는 명령줄에 해당 위치에 지정 된 것 처럼 명령 파일 입력을 허용 합니다. 명령 파일을 중첩할 수 없습니다. 링크 하지 않는 한 명령 파일의 내용을 에코 합니다 [/NOLOGO](../../build/reference/nologo-suppress-startup-banner-linker.md) 옵션을 지정 합니다.

## <a name="example"></a>예제

DLL을 작성 하려면 다음 명령을 명령 파일에 있는 개체 파일 및 라이브러리의 이름을 전달 하 고 세 번째 /EXPORTS 옵션의 사양에 대 한 파일에 명령을 사용 하 여 키를 누릅니다.

```cmd
link /dll @objlist.txt @liblist.txt @exports.txt
```

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)   
[링커 옵션](../../build/reference/linker-options.md)