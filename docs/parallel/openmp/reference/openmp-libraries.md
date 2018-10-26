---
title: OpenMP 라이브러리 | Microsoft Docs
ms.custom: ''
ms.date: 10/24/2018
ms.technology:
- cpp-parallel
ms.topic: reference
dev_langs:
- C++
ms.assetid: f89abf97-67e3-4327-bc30-43f85b9533a2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7620b0ea710a5474fbbbf614691ceeb1e5cc945e
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50062004"
---
# <a name="openmp-libraries"></a>OpenMP 라이브러리

Visual c + +의 OpenMP 런타임 라이브러리를 구성 하는.lib 파일에 설명 합니다.

다음 라이브러리는 Visual c + + OpenMP에서 런타임 라이브러리 함수를 포함 합니다.

|OpenMP에서 런타임 라이브러리|특성|
|------------------------------|---------------------|
|VCOMP.LIB|다중 스레드, 동적 링크 (VCOMP에 대 한 가져오기 라이브러리입니다. LIB)입니다.|
|VCOMPD.LIB|다중 스레드, 동적 링크 (VCOMPD에 대 한 가져오기 라이브러리입니다. 커버) (디버그)|

컴파일에서 _DEBUG이 정의 하는 경우 `#include omp.h` VCOMPD 소스 코드에 있습니다. LIB 기본 lib이 됩니다. 그렇지 않으면 VCOMP 합니다. LIB 사용 됩니다.

사용할 수 있습니다 [/NODEFAULTLIB (라이브러리 무시)](../../../build/reference/nodefaultlib-ignore-libraries.md) 기본 lib 제거한 사용자가 선택한 라이브러리를 사용 하 여 명시적으로 연결 합니다.

OpenMP Dll Visual c + + 재배포 가능 패키지 디렉터리에 있으며 OpenMP를 사용 하는 응용 프로그램과 함께 배포 해야 합니다.

## <a name="see-also"></a>참고자료

[라이브러리 참조](openmp-library-reference.md)
