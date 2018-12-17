---
title: 바이트 인덱스
ms.date: 11/04/2016
helpviewer_keywords:
- MBCS [C++], byte indices
- byte indices [C++]
ms.assetid: f6e7774a-86c6-41c2-89e3-74fd46432e47
ms.openlocfilehash: 4e19868e5297e1c1615efabde2aee418bc53c51e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50448817"
---
# <a name="byte-indices"></a>바이트 인덱스

다음 팁을 사용하십시오.

- 문자열에 대한 바이트 단위 인덱스 작업은 포인터 조작에서 나타나는 것과 유사한 문제를 발생시킵니다. 문자열에서 백슬래시 문자를 검색하는 다음 예제를 보십시오.

    ```cpp
    while ( rgch[ i ] != '\\' )
        i++;
    ```

   위 예제에서는 선행 바이트가 아니라 후행 바이트를 인덱스할 수 있으므로 `character`를 가리키지 않을 수 있습니다.

- [_mbclen](../c-runtime-library/reference/mbclen-mblen-mblen-l.md) 함수를 사용하여 앞의 문제를 해결합니다:

    ```cpp
    while ( rgch[ i ] != '\\' )
        i += _mbclen ( rgch + i );
    ```

   이렇게 하면 선행 바이트에 대해 올바로 인덱싱되므로 `character`를 가리키게 됩니다. `_mbclen` 함수는 문자 크기(1바이트 또는 2바이트)를 결정합니다.

## <a name="see-also"></a>참고 항목

[MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[문자열의 마지막 문자](../text/last-character-in-a-string.md)
