---
title: 스텁 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- STUB
dev_langs:
- C++
helpviewer_keywords:
- STUB .def file statement
ms.assetid: 0a3b9643-19ed-47e9-8173-ee16bc8ed056
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 151d7b425a7f397a05e3a06e9d94489a0c76f899
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45725116"
---
# <a name="stub"></a>STUB

(WINNT에 정의 된 IMAGE_DOS_HEADER 구조를 포함 하는 파일 이름을 지정할 수 있습니다 (VxD), 가상 장치 드라이버를 작성 하는 모듈 정의 파일에 사용 되는 경우. H) 기본 헤더 대신 가상 장치 드라이버 (VxD)에서 사용 되는 합니다.

```
STUB:filename
```

## <a name="remarks"></a>설명

지정 하는 해당 하는 방법은 *filename* 사용 하는 것은 [스텁](../../build/reference/stub-ms-dos-stub-file-name.md) 링커 옵션입니다.

STUB은 VxD를 빌드할 때에 모듈 정의 파일에서 유효 합니다.

## <a name="see-also"></a>참고 항목

[모듈 정의 문의 규칙](../../build/reference/rules-for-module-definition-statements.md)