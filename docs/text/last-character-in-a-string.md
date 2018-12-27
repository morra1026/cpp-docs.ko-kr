---
title: 문자열의 마지막 문자
ms.date: 11/04/2016
helpviewer_keywords:
- last character in string
- MBCS [C++], last character in string
ms.assetid: 0a180376-4e55-41e8-9c64-539c7b6d8047
ms.openlocfilehash: 535c2e58edab49e0e2a9dbc3fce9821d5909f1c5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50456266"
---
# <a name="last-character-in-a-string"></a>문자열의 마지막 문자

멀티바이트 문자 집합의 문자를 판단하기 위해 이 내용을 참고하세요.

- 후행 바이트는 대부분 ASCII 문자 집합의 범위와 겹칩니다. ASCII 문자 중 값이 32보다 작은 경우 제어 문자에 해당하는데, 바이트 스캔을 할 경우 안전하게 사용할 수 있는 방법이 있습니다.

- 문자열의 마지막이 백슬래시 문자인지 확인하는 코드를 한번 생각해 보세요.

    ```cpp
    if ( sz[ strlen( sz ) - 1 ] == '\\' )    // Is last character a '\'?
        // . . .
    ```

   `strlen`은 MBCS를 고려해 인식하지 않고 무조건 바이트 수를 반환합니다. 일부 코드 페이지(예: 932)의 경우, '\\'(0x5c)는 유효한 후행 바이트입니다(`sz`는 C문자열).

   한 가지 해결책이 같습니다. 이러한 방식으로 코드를 다시 작성

    ```cpp
    char *pLast;
    pLast = _mbsrchr( sz, '\\' );    // find last occurrence of '\' in sz
    if ( pLast && ( *_mbsinc( pLast ) == '\0' ) )
        // . . .
    ```

   이 코드에서는 MBCS 함수 `_mbsrchr` 고 `_mbsinc`입니다. 이러한 함수의 MBCS 인식 이기 때문에 이러한 구분할 수는 '\\'문자와 후행 바이트'\\'. 코드는 문자열의 마지막 문자 ('\0') null 인 경우 일부 작업을 수행 합니다.

## <a name="see-also"></a>참고 항목

[MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[문자 할당](../text/character-assignment.md)