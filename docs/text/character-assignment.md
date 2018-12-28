---
title: 문자 할당
ms.date: 11/04/2016
helpviewer_keywords:
- characters [C++], assignments
- MBCS [C++], character assignments
ms.assetid: dcc329cd-92df-4e20-817d-364be62ff28f
ms.openlocfilehash: 9099382a212f9f7bd6c071f4e4d9a0c2bc8887de
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50435375"
---
# <a name="character-assignment"></a>문자 할당

문자열을 복사하는 다음의 예제를 살펴봅시다. **while** 루프가 문자열을 순회하면서 'X'를 제외한 모든 문자를 다른 문자열로 복사하고 있습니다.

```cpp
while( *sz2 )
{
    if( *sz2 != 'X' )
        *sz1++ = *sz2++;
    else
        sz2++;
}
```

이 코드는 sz2에 있는 바이트를 sz1이 가리키는 위치로 복사한 다음 sz1을 증가시켜 다음 바이트를 가져옵니다. 그러나 sz2의 다음 문자가 더블바이트 문자인 경우 sz1에 대한 할당은 첫 번째 바이트만 복사가 이루어집니다. 다음 코드는 문자를 안전하게 복사하고 sz1과 sz2를 올바르게 증가시킵니다.

```cpp
while( *sz2 )
{
    if( *sz2 != 'X' )
    {
        _mbscpy_s( sz1, 1, sz2 );
        sz1 = _mbsinc( sz1 );
        sz2 = _mbsinc( sz2 );
    }
    else
        sz2 = _mbsinc( sz2 );
}
```

## <a name="see-also"></a>참고 항목

[MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[문자 비교](../text/character-comparison.md)
