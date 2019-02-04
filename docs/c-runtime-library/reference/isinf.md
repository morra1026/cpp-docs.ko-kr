---
title: isinf
ms.date: 01/31/2019
f1_keywords:
- isinf
- math/isinf
helpviewer_keywords:
- isinf function
ms.openlocfilehash: be99970a0c7b152ba213eabd59b53a7503cd3c54
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55703473"
---
# <a name="isinf"></a>isinf

부동 소수점 값을 무한대 인지 확인 합니다.

## <a name="syntax"></a>구문

```C
int isinf(
   /* floating-point */ x
); /* C-only macro */

template <class FloatingType>
inline bool isinf(
   FloatingType x
) throw(); /* C++-only template function */
```

### <a name="parameters"></a>매개 변수

*x*<br/>
테스트할 부동 소수점 값입니다.

## <a name="return-value"></a>반환 값

**isinf** 0이 아닌 값을 반환 합니다 (**true** c + + 코드에서) 하는 경우 인수 *x* 는 양수 또는 음수 무한대. **isinf** 0을 반환 합니다 (**false** c + + 코드에서) 인수가 유한 인 경우 또는 NAN입니다. 일반 및 subnormal 부동 소수점 값은 유한 간주 됩니다.

## <a name="remarks"></a>설명

**isinf** 는 C 및 c + +로 컴파일할 때 인라인 템플릿 함수를 컴파일할 때 매크로입니다.

## <a name="requirements"></a>요구 사항

|기능|필수 헤더(C)|필수 헤더(C++)|
|--------------|---------------------------|-------------------------------|
|**isinf**|\<math.h>|\<math.h> 또는 \<cmath>|

호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="see-also"></a>참고자료

[부동 소수점 지원](../../c-runtime-library/floating-point-support.md)<br/>
[fpclassify](fpclassify.md)<br/>
[_fpclass, _fpclassf](fpclass-fpclassf.md)<br/>
[isfinite, _finite, _finitef](finite-finitef.md)<br/>
[isnan, _isnan, _isnanf](isnan-isnan-isnanf.md)<br/>
[isnormal](isnormal.md)<br/>
