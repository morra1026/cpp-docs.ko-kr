---
title: /IMPORTS(DUMPBIN)
ms.date: 11/04/2016
f1_keywords:
- /imports
helpviewer_keywords:
- IMPORTS dumpbin option
- /IMPORTS dumpbin option
- -IMPORTS dumpbin option
ms.assetid: 6a296216-2b1b-40f8-8736-cd4553a22456
ms.openlocfilehash: 9367457a8e7f6be1f372244f8288a994eb777071
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50613787"
---
# <a name="imports-dumpbin"></a>/IMPORTS(DUMPBIN)

```
/IMPORTS[:file]
```

이 옵션에는 Dll 목록을 표시 (정적 연결 모두 및 [지연 로드](../../build/reference/linker-support-for-delay-loaded-dlls.md))에서 이러한 각 Dll 실행 파일 또는 DLL 및 모든 개별 가져오기도 가져올 수 있는 합니다.

선택적 `file` 사양을 사용 하면는 해당 DLL에 대 한 가져오기를 표시 되도록 지정할 수 있습니다. 예를 들어:

```
dumpbin /IMPORTS:msvcrt.dll
```

## <a name="remarks"></a>설명

이 옵션으로 표시 되는 출력은 비슷합니다는 [내보냅니다/](../../build/reference/dash-exports.md) 출력 합니다.

만 [/HEADERS](../../build/reference/headers.md) DUMPBIN 옵션을 사용 하 여 생성 된 파일에 사용할 수 있습니다 합니다 [/GL](../../build/reference/gl-whole-program-optimization.md) 컴파일러 옵션입니다.

## <a name="see-also"></a>참고 항목

[DUMPBIN 옵션](../../build/reference/dumpbin-options.md)