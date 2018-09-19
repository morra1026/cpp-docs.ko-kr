---
title: CL 명령 파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- cl
dev_langs:
- C++
helpviewer_keywords:
- cl.exe compiler, command files
- command files
- command files, CL compiler
ms.assetid: ec3cea06-2af0-4fe9-a94c-119c9d31b3a9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8458462304a9b739c61997505724d21bb56763f6
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45708672"
---
# <a name="cl-command-files"></a>CL 명령 파일

명령 파일은 옵션과 그렇지 않은 경우에 입력 하는 파일 이름이 포함 된 텍스트 파일을 [명령줄](../../build/reference/compiler-command-line-syntax.md) 사용 하 여 지정 하거나 합니다 [CL 환경 변수](../../build/reference/cl-environment-variables.md). Cl 컴파일러 명령 파일을 명령줄 또는 CL 환경 변수에서를 인수로 사용 합니다. 명령줄이나 CL 환경 변수와는 달리 명령 파일을 사용하면 여러 줄로 구성된 옵션과 파일 이름을 사용할 수 있습니다.

옵션 및 명령 파일의 파일 이름을 CL 환경 변수 내에서 또는 명령줄에서 명령 파일의 위치에 따라 처리 됩니다. 그러나 /link 옵션에 표시 되 면 명령 파일 줄의 나머지 부분에서 모든 옵션을 링커에 전달 됩니다. 명령 파일의 다음 줄의 옵션 및 옵션은 명령줄에서 명령 파일 호출 후 컴파일러 옵션으로 인식 됩니다. 옵션의 순서에 대 한 해석은 미치는 영향에 대 한 자세한 내용은 참조 하세요. [CL 옵션 순서](../../build/reference/order-of-cl-options.md)합니다.

명령 파일 CL 명령을 사용할 수 없습니다. 각 옵션 시작 하 고 끝나야 하며 같은 줄에서 백슬래시를 사용할 수 없습니다 (**\\**) 두 줄 옵션을 결합 합니다.

명령 파일 된는 at 기호 (**\@**) 뒤에 파일 이름이; 파일 이름에는 절대 또는 상대 경로 지정할 수 있습니다.

예를 들어 응답 파일에 다음 명령입니다.

```
/Og /link LIBC.LIB
```

고 CL 명령을 지정 합니다.

```
CL /Ob2 @RESP MYAPP.C
```

CL 명령을 아래와 같습니다.

```
CL /Ob2 /Og MYAPP.C /link LIBC.LIB
```

Note 명령줄 명령과 명령 파일 관리자에 게는 효과적으로 결합 됩니다.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[컴파일러 옵션](../../build/reference/compiler-options.md)