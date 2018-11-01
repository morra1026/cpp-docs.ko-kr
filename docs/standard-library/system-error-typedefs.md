---
title: '&lt;system_error&gt; 형식 정의'
ms.date: 11/04/2016
f1_keywords:
- system_error/std::generic_errno
ms.assetid: 28cf9f7d-9c28-4baa-a297-67c8260b07fb
ms.openlocfilehash: 95b2cb22d4fbff4f92cf28041e70ae599c318cbc
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50531058"
---
# <a name="ltsystemerrorgt-typedefs"></a>&lt;system_error&gt; 형식 정의

||
|-|
|[generic_errno](#generic_errno)|

## <a name="generic_errno"></a>  generic_errno

`<errno.h>`에서 Posix에 의해 정의되는 모든 오류 코드 매크로의 심볼 이름을 제공하는 열거형을 나타내는 형식입니다.

```cpp
typedef errc generic_error;
```

### <a name="remarks"></a>설명

이 형식은 [errc](../standard-library/system-error-enums.md#errc)와 동일한 의미입니다.

## <a name="see-also"></a>참고자료

[<system_error>](../standard-library/system-error.md)<br/>
