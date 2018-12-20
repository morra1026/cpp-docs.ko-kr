---
title: 문자단위로 포인터 값 증감 시키기
ms.date: 11/04/2016
helpviewer_keywords:
- incrementing pointers
- MBCS [C++], pointers
- pointers [C++], multibyte characters
- decrementing pointers
ms.assetid: 0872b4a0-e2bd-4004-8319-070efb76f2fd
ms.openlocfilehash: 1899e3153300bbfbfce068d29351de601f336b6d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50567091"
---
# <a name="incrementing-and-decrementing-pointers"></a>문자단위로 포인터 값 증감 시키기

멀티바이트 문자 집합(MBCS) 환경에서 문자열을 가리키는 포인터 값을 증가시키고 감소시킨다면 다음 내용을 참고합니다.

- 포인터를 이용해 문자열을 가리키고 있다면 후행 바이트가 아닌 선행 바이트를 가리켜야 합니다. 일반적으로 후행 바이트를 가리키고 있는 포인터는 안전하지 않습니다. 또한 역방향 보다는 순방향으로 문자열 검색하는 것이 안전합니다.

- 문자단위로 포인터 값을 움직여 포인터를 증가시키고 감소시키는 함수와 매크라고 있습니다.

    ```cpp
    sz1++;
    ```

   다음 처럼 사용하세요.

    ```cpp
    sz1 = _mbsinc( sz1 );
    ```

   `_mbsinc`와 `_mbsdec` 함수는 문자의 크기와 관계없이 포인터를 `문자` 단위로 올바르게 증가, 감소시킵니다.

- 감소의 경우 다음과 같이 문자열의 헤드에 대한 포인터가 필요합니다.

    ```cpp
    sz2--;
    ```

   다음과 같이 사용하십시요.

    ```cpp
    sz2 = _mbsdec( sz2Head, sz2 );
    ```

   헤드 포인터가 문자열에서 유효한 문자가 됩니다.

    ```cpp
    sz2Head < sz2
    ```

   포인터는 선행 바이트 값 범위 안에 있는 유효한 포인터야 합니다.

- `_mbsdec`를 호출하는 것에 대한 더 빠른 성능을 얻고 싶다면 이전 문자에 대한 포인터를 유지하는 것도 한 방법입니다.

## <a name="see-also"></a>참고 항목

[멀티바이트 문자 집합(MBCS) 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[바이트 인덱스](../text/byte-indices.md)
