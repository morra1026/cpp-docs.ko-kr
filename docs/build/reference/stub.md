---
title: STUB
ms.date: 11/04/2016
f1_keywords:
- STUB
helpviewer_keywords:
- STUB .def file statement
ms.assetid: 0a3b9643-19ed-47e9-8173-ee16bc8ed056
ms.openlocfilehash: fd2e7c4a3bd9fa09b88f4c3caa9b7d5b73c1ad98
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57412941"
---
# <a name="stub"></a>STUB

(WINNT에 정의 된 IMAGE_DOS_HEADER 구조를 포함 하는 파일 이름을 지정할 수 있습니다 (VxD), 가상 장치 드라이버를 작성 하는 모듈 정의 파일에 사용 되는 경우. H) 기본 헤더 대신 가상 장치 드라이버 (VxD)에서 사용 되는 합니다.

```
STUB:filename
```

## <a name="remarks"></a>설명

지정 하는 해당 하는 방법은 *filename* 사용 하는 것은 [스텁](../../build/reference/stub-ms-dos-stub-file-name.md) 링커 옵션입니다.

STUB은 VxD를 빌드할 때에 모듈 정의 파일에서 유효 합니다.

## <a name="see-also"></a>참고자료

[모듈 정의 문의 규칙](../../build/reference/rules-for-module-definition-statements.md)
