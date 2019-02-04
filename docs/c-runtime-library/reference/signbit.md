---
title: signbit
ms.date: 01/31/2019
f1_keywords:
- signbit
- math/signbit
helpviewer_keywords:
- signbit function
ms.openlocfilehash: ce2f632f11296bf71036011a57f242365951d7f2
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55703459"
---
# <a name="signbit"></a>signbit

부동 소수점 값이 음수 인지를 결정 합니다.

## <a name="syntax"></a>구문

```C
int signbit(
   /* floating-point */ x
); /* C-only macro */

inline bool signbit(
   float x
) throw(); /* C++-only overloaded function */

inline bool signbit(
   double x
) throw(); /* C++-only overloaded function */

inline bool signbit(
   long double x
) throw(); /* C++-only overloaded function */
```

### <a name="parameters"></a>매개 변수

*x*<br/>
테스트할 부동 소수점 값입니다.

## <a name="return-value"></a>반환 값

**signbit** 0이 아닌 값을 반환 합니다 (**true** c + +에서) 하는 경우 인수 *x* 는 음수 또는 음수 무한대. 0을 반환 합니다 (**false** c + +에서) 인수가 음수가 아닌, 양의 무한대 또는 NAN 인 경우.

## <a name="remarks"></a>설명

**signbit** 는 C 및 c + +로 컴파일된 경우 오버 로드 된 인라인 함수를 컴파일할 때 매크로입니다.

## <a name="requirements"></a>요구 사항

|기능|필수 헤더(C)|필수 헤더(C++)|
|--------------|---------------------------|-------------------------------|
|**signbit**|\<math.h>|\<math.h> 또는 \<cmath>|

호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="see-also"></a>참고자료

[부동 소수점 지원](../../c-runtime-library/floating-point-support.md)<br/>
[isfinite, _finite, _finitef](finite-finitef.md)<br/>
[isinf](isinf.md)<br/>
[isnan, _isnan, _isnanf](isnan-isnan-isnanf.md)<br/>
[isnormal](isnormal.md)<br/>
[_fpclass, _fpclassf](fpclass-fpclassf.md)<br/>
