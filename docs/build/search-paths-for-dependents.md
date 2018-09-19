---
title: 종속 항목에 대 한 경로 검색 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- NMAKE program, dependents
- dependents, NMAKE
ms.assetid: bf998e47-da74-48b5-891d-d3d8ce57264b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d1fd407f99abb98fb949b6d5bcc45b10c6ff9121
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706308"
---
# <a name="search-paths-for-dependents"></a>종속 파일의 경로 검색

각 종속 파일에 선택적 검색 경로 다음과 같이 지정 합니다.

## <a name="syntax"></a>구문

```
{directory[;directory...]}dependent
```

## <a name="remarks"></a>설명

NMAKE는 먼저 현재 디렉터리에서에서 찾은 다음 지정한 순서에 따라 디렉터리에서 종속 찾습니다. 매크로 일부 또는 전체 검색 경로를 지정할 수 있습니다. 디렉터리 이름은 묶고 중괄호 ({}); 세미콜론 (;)를 사용 하 여 여러 디렉터리를 구분 합니다. 공백 또는 탭 허용 됩니다.

## <a name="see-also"></a>참고 항목

[종속 파일](../build/dependents.md)