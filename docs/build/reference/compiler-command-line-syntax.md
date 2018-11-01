---
title: 컴파일러 명령줄 구문
ms.date: 11/04/2016
helpviewer_keywords:
- syntax, CL compiler command line
- cl.exe compiler, command-line syntax
ms.assetid: acba2c1c-0803-4a3a-af25-63e849b930a2
ms.openlocfilehash: a350a2cb793630b90143b7d190ada9469a79bfc1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50581300"
---
# <a name="compiler-command-line-syntax"></a>컴파일러 명령줄 구문

CL 명령줄 구문을 사용합니다.

```
CL [option...] file... [option | file]... [lib...] [@command-file] [/link link-opt...]
```

다음 표에 CL 명령 입력 합니다.

|입력|의미|
|-----------|-------------|
|*옵션*|하나 이상의 [CL 옵션](../../build/reference/compiler-options.md)합니다. 모든 옵션이 모든 지정 된 소스 파일에 적용 되는 참고 합니다. 옵션은 슬래시 (/) 또는 대시 (-)으로 지정 됩니다. 옵션 인수는 옵션의 설명 문서 옵션 및 인수 사이 공백을 허용 되는지 여부 하는 경우. /HELP 옵션) (제외 옵션 이름은 대/소문자를 구분 합니다. 참조 [CL 옵션 순서](../../build/reference/order-of-cl-options.md) 자세한 내용은 합니다.|
|`file`|하나 이상의 소스 파일,.obj 파일 또는 라이브러리의 이름입니다. CL 소스 파일을 컴파일한.obj 파일 및 라이브러리의 이름을 링커에 전달 합니다. 참조 [CL 파일 이름 구문](../../build/reference/cl-filename-syntax.md) 자세한 내용은 합니다.|
|*lib*|하나 이상의 라이브러리 이름입니다. CL 이러한 이름을 링커에 전달합니다.|
|*명령 파일*|여러 옵션 및 파일 이름을 포함 하는 파일입니다. 참조 [CL 명령 파일](../../build/reference/cl-command-files.md) 자세한 내용은 합니다.|
|*링크-opt*|하나 이상의 [링커 옵션](../../build/reference/linker-options.md)합니다. CL 이러한 옵션을 링커에 전달 합니다.|

옵션, 파일 이름 및 라이브러리 이름과 임의 개수의 명령줄에서 문자 수가 1024, 운영 체제에서 결정 한도 넘지 않는으로 지정할 수 있습니다.

Cl.exe의 반환 값에 대 한 정보를 참조 하세요 [cl.exe의 반환 값](../../build/reference/return-value-of-cl-exe.md) 합니다.

> [!NOTE]
>  Windows의 이후 릴리스에서 동일 하 게 유지 하는 1024 자로 제한 된 명령줄 입력된 보장 되지 않습니다.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[컴파일러 옵션](../../build/reference/compiler-options.md)