---
title: 문자 비교
ms.date: 11/04/2016
helpviewer_keywords:
- comparing characters
- MBCS [C++], character comparison
- characters [C++], comparing
ms.assetid: 18846e44-3e6e-40c4-9b42-3153fb15db20
ms.openlocfilehash: 206910d4b76f93a92ee5230a227d6f0346a85e61
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50615412"
---
# <a name="character-comparison"></a>문자 비교

다음 팁을 사용하십시오.

- 알려진 선행 바이트와 ASCII 문자 비교는 제대로 수행됩니다.

    ```cpp
    if( *sz1 == 'A' )
    ```

- 두 개의 알 수 없는 문자를 비교하려면 Mbstring.h에 정의된 매크로 중 하나를 사용해야 합니다.

    ```cpp
    if( !_mbccmp( sz1, sz2) )
    ```

   이렇게 하면 더블바이트 문자의 바이트 두 개가 모두 비교됩니다.

## <a name="see-also"></a>참고 항목

[MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[버퍼 오버플로](../text/buffer-overflow.md)