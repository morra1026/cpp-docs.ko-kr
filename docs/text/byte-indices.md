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

문자의 바이트 길이를 알고 싶다면 다음의 내용을 참고하세요.

- 포인터 조작에서 나타나는 것과 유사한 문제를 표시하는 문자열로 바이트 단위 인덱스를 사용합니다. 백슬래시 문자에 대한 문자열을 검사하는 다음 예제를 살펴보세요.

    ```cpp
    while ( rgch[ i ] != '\\' )
        i++;
    ```

   이렇게 인덱싱한다면 선행 바이트가 아닌 후행 바이트를 인덱싱할 수 있으므로 올바른 `character`를 얻지 못할 수 있습니다.

- 이런 문제를 해결하려면 [_mbclen](../c-runtime-library/reference/mbclen-mblen-mblen-l.md)함수를 사용하세요.

    ```cpp
    while ( rgch[ i ] != '\\' )
        i += _mbclen ( rgch + i );
    ```

   이렇게 하면 선행 바이트를 인덱싱하여 올바른 `character`를 얻을 수 있습니다. `_mbclen` 함수는 1바이트인지 2 바이트인지에 대한 크기를 판단하여 처리합니다.

## <a name="see-also"></a>참고 항목

[멀티바이트 문자 집합(MBCS) 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[문자열의 마지막 문자](../text/last-character-in-a-string.md)
