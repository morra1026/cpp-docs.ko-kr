---
title: -LINENUMBERS | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /linenumbers
dev_langs:
- C++
helpviewer_keywords:
- LINENUMBERS dumpbin option
- line numbers
- -LINENUMBERS dumpbin option
- /LINENUMBERS dumpbin option
ms.assetid: 1681d582-2c2f-484e-9920-109959549055
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c9b969f51733d9eb4c45ac5609b42920765a7ad5
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45704056"
---
# <a name="linenumbers"></a>/LINENUMBERS

```
/LINENUMBERS
```

## <a name="remarks"></a>설명

이 옵션에는 COFF 줄 번호가 표시 됩니다. C7 호환 프로그램 데이터베이스 (/Zi)을 사용 하 여 컴파일된 개체 파일에 있는 줄 번호 (/ Z7), 또는 줄 번호만 (/Zd). 실행 파일 또는 DLL 디버그 정보 생성을 사용 하 여 연결 된 경우 COFF 줄 번호 포함 (/debug).

만 [/HEADERS](../../build/reference/headers.md) DUMPBIN 옵션을 사용 하 여 생성 된 파일에 사용할 수 있습니다 합니다 [/GL](../../build/reference/gl-whole-program-optimization.md) 컴파일러 옵션입니다.

## <a name="see-also"></a>참고 항목

[DUMPBIN 옵션](../../build/reference/dumpbin-options.md)