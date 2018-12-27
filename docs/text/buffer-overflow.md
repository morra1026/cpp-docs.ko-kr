---
title: 버퍼 오버플로
ms.date: 11/04/2016
helpviewer_keywords:
- buffers [C++], character sizes
- buffer overflows [C++]
- MBCS [C++], buffer overflow
ms.assetid: f2b7e40a-f02b-46d8-a449-51d26fc0c663
ms.openlocfilehash: 97488f3023481c20599e8cf5201fbce68dd23516
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50566503"
---
# <a name="buffer-overflow"></a>버퍼 오버플로

다양한 문자 크기를 갖는 문자를 버퍼에 넣을 때 문제가 발생할 수 있습니다. 문자열 `sz`의 문자를 `rgch`버퍼에 복사하는 다음 코드를 살펴봅시다.

```cpp
cb = 0;
while( cb < sizeof( rgch ) )
    rgch[ cb++ ] = *sz++;
```

마지막 바이트가 복사될 때 선행 바이트만 복사된 것인지 의문을 가져야 합니다. 다음 예는 버퍼 오버플로가 발생할 수 있으므로 문제가 해결된 것은 아닙니다.

```cpp
cb = 0;
while( cb < sizeof( rgch ) )
{
    _mbccpy( rgch + cb, sz );
    cb += _mbclen( sz );
    sz = _mbsinc( sz );
}
```

`_mbccpy` 호출 올바른 작업을 수행 하려고 합니다.-1 또는 2 바이트 인지 전체 문자를 복사 합니다. 하지만 문자가 2 바이트 이면 복사할 마지막 문자 버퍼에 들어가지 않을 수 있다는 것을 고려 하지 않습니다. 올바른 솔루션이 다음과 같습니다.

```cpp
cb = 0;
while( (cb + _mbclen( sz )) <= sizeof( rgch ) )
{
    _mbccpy( rgch + cb, sz );
    cb += _mbclen( sz );
    sz = _mbsinc( sz );
}
```

이 코드는 루프에서 가능한 버퍼 오버플로 대 한 테스트 사용 하 여 테스트할 `_mbclen` 에서 가리키는 현재 문자 크기를 테스트 하려면 `sz`합니다. 호출 하 여는 `_mbsnbcpy` 함수에서 코드를 바꿀 수 있습니다 합니다 **하는 동안** 단일 코드 줄을 사용 하 여 루프입니다. 예를 들어:

```cpp
_mbsnbcpy( rgch, sz, sizeof( rgch ) );
```

## <a name="see-also"></a>참고 항목

[MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)