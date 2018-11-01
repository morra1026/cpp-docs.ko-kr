---
title: is_error_code_enum 구조체
ms.date: 11/04/2016
f1_keywords:
- future/std::is_error_code_enum
ms.assetid: 84ae4b99-66d2-41ba-9b50-645fcbe14630
ms.openlocfilehash: 54def287aa6b4bbb06d88006615b5df45b482051
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50676423"
---
# <a name="iserrorcodeenum-structure"></a>is_error_code_enum 구조체

[future_errc](../standard-library/future-enums.md#future_errc)가 [error_code](../standard-library/error-code-class.md)를 저장하는 데 적합함을 나타내는 특수화입니다.

## <a name="syntax"></a>구문

```cpp
template <>
struct is_error_code_enum<Future_errc> : public true_type;
```

## <a name="requirements"></a>요구 사항

**헤더:** \<향후 >

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)<br/>
[\<future>](../standard-library/future.md)<br/>
