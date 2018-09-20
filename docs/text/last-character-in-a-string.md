---
title: 문자열의 문자를 지난 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- last character in string
- MBCS [C++], last character in string
ms.assetid: 0a180376-4e55-41e8-9c64-539c7b6d8047
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e207ec1d5489a629b765d398e26ac7c07771d0da
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46384990"
---
# <a name="last-character-in-a-string"></a>문자열의 마지막 문자

다음 팁을 사용 합니다.

- 후행 바이트 범위에는 ASCII 문자를 집합 대부분에서 겹칩니다. 제어 문자 (32 보다 작은)에 대 한 바이트 단위 검색을 안전 하 게 사용할 수 있습니다.

- 문자열의 마지막 문자는 백슬래시 문자 있는지를 확인할 수 있습니다 하는 코드를 다음 줄을 고려 합니다.

    ```cpp
    if ( sz[ strlen( sz ) - 1 ] == '\\' )    // Is last character a '\'?
        // . . .
    ```

   때문에 `strlen` MBCS 인식 하지 않는 멀티 바이트 문자열의 문자 수가 바이트의 수를 반환 합니다. 또한 이때 일부 코드 페이지 (예: 932), '\\' (0x5c)는 유효한 후행 바이트 (`sz` 은 C 문자열)입니다.

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