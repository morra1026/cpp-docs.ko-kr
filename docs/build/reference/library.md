---
title: 라이브러리 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- LIBRARY
dev_langs:
- C++
helpviewer_keywords:
- LIBRARY .def file statement
ms.assetid: 1d7ccc92-e088-4ef7-9ef0-25c3862cc051
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 43b14e8e8ff4871ba4319c7f4fac5545e72e710b
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45723556"
---
# <a name="library"></a>LIBRARY

DLL을 만들려면 링크를 알려 줍니다. 동시에, 링크 빌드에서.exp 파일을 사용 하지 않으면 가져오기 라이브러리를 만듭니다.

```
LIBRARY [library][BASE=address]
```

## <a name="remarks"></a>설명

합니다 *라이브러리* 인수는 DLL의 이름을 지정 합니다. 사용할 수도 있습니다는 [/출력](../../build/reference/out-output-file-name.md) DLL의 출력 이름을 지정 하는 링커 옵션입니다.

기본 =*주소* 인수 운영 체제에서 DLL을 로드 하는 데 사용 하는 기본 주소를 가져오거나 설정 합니다. 이 인수는 0x10000000의 기본 DLL 위치를 재정의합니다. 에 대 한 설명을 참조는 [/base](../../build/reference/base-base-address.md) 기본 주소에 대 한 세부 정보에 대 한 옵션입니다.

사용 해야 합니다 [/DLL](../../build/reference/dll-build-a-dll.md) DLL을 빌드할 때 링커 옵션입니다.

## <a name="see-also"></a>참고 항목

[모듈 정의 문의 규칙](../../build/reference/rules-for-module-definition-statements.md)