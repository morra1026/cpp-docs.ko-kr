---
title: 필요한 값 계산
ms.date: 11/04/2016
helpviewer_keywords:
- helper functions, calculating necessary values
ms.assetid: 4f037d0f-881a-4a48-a9d2-9f8872dfccb7
ms.openlocfilehash: 80c028a315669fb0032628bb86a834d429935f50
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50513869"
---
# <a name="calculating-necessary-values"></a>필요한 값 계산

두 가지 중요 한 정보는 지연 도우미 루틴에 의해 계산 해야 합니다. 이 위해 두 개의 인라인 함수의에서 경우이 정보를 계산 하는 데 delayhlp.cpp

- 첫 번째 계산에서 현재 가져오기 (가져오기 주소 테이블 (IAT), 바인딩된 가져오기 주소 테이블 (BIAT) 및 바인딩되지 않은 가져오기 주소 테이블 (uiat 언바인딩 된))의 세 가지 테이블의 인덱스입니다.

- 두 번째 함수는 유효한 IAT에서 가져오기의 수를 셉니다.

```cpp
// utility function for calculating the index of the current import
// for all the tables (INT, BIAT, UIAT, and IAT).
__inline unsigned
IndexFromPImgThunkData(PCImgThunkData pitdCur, PCImgThunkData pitdBase) {
    return pitdCur - pitdBase;
    }

// utility function for calculating the count of imports given the base
// of the IAT. NB: this only works on a valid IAT!
__inline unsigned
CountOfImports(PCImgThunkData pitdBase) {
    unsigned        cRet = 0;
    PCImgThunkData  pitd = pitdBase;
    while (pitd->u1.Function) {
        pitd++;
        cRet++;
        }
    return cRet;
    }
```

## <a name="see-also"></a>참고 항목

[도우미 함수 이해](understanding-the-helper-function.md)