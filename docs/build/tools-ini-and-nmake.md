---
title: Tools.ini와 NMAKE
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, reading files
- Tools.ini and NMake
ms.assetid: ebd5eab6-ddf4-430e-bf4a-1db5bb84e344
ms.openlocfilehash: 1a8673741cb49c504855fb1af00dbdc06379210d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50654417"
---
# <a name="toolsini-and-nmake"></a>Tools.ini와 NMAKE

NMAKE 읽습니다 Tools.ini 메이크파일에 읽기 전에 /R 사용 되지 않은 경우. 찾습니다 Tools.ini 먼저 현재 디렉터리에서 찾은 다음 INIT 환경 변수로 지정 된 디렉터리에서. NMAKE 설정 초기화 파일의 섹션으로 시작 `[NMAKE]` 한 메이크파일의 정보를 포함할 수 있습니다. 숫자 기호를 사용 하 여 시작 하는 별도 줄에 주석 지정 (#).

## <a name="see-also"></a>참고 항목

[NMAKE 실행](../build/running-nmake.md)