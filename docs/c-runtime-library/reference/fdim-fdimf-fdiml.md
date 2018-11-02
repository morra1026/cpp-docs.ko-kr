---
title: fdim, fdimf, fdiml
ms.date: 04/05/2018
apiname:
- fdim
- fdimf
- fdiml
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- fdim
- fdimf
- fdiml
- math/fdim
- math/fdimf
- math/fdiml
helpviewer_keywords:
- fdim function
- fdimf function
- fdiml function
ms.assetid: 2d4ac639-51e9-462d-84ab-fb03b06971a0
ms.openlocfilehash: d8cea831e333ebcd9677d830641c60e460ba5ed4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50515091"
---
# <a name="fdim-fdimf-fdiml"></a>fdim, fdimf, fdiml

첫 번째 값과 두 번째 값의 양의 차이를 결정합니다.

## <a name="syntax"></a>구문

```C
double fdim(
   double x,
   double y
);

float fdim(
   float x,
   float y
); //C++ only

long double fdim(
   long double x,
   long double y
); //C++ only

float fdimf(
   float x,
   float y
);

long double fdiml(
   long double x,
   long double y
);

```

### <a name="parameters"></a>매개 변수

*x*<br/>
첫 번째 값입니다.

*y*<br/>
두 번째 값입니다.

## <a name="return-value"></a>반환 값

양의 차이 반환 *x* 하 고 *y*:

|반환 값|시나리오|
|------------------|--------------|
|x-y|if x > y|
|0|if x <= y|

그렇지 않으면 다음 오류 중 하나를 반환할 수 있습니다.

|문제|반환|
|-----------|------------|
|오버플로 범위 오류|+HUGE_VAL, +HUGE_VALF 또는 +HUGE_VALL|
|언더플로 범위 오류|올바른 값(반올림 후)|
|*x* 나 *y* 가 NaN|NaN|

오류는 [_matherr](matherr.md)에 지정된 대로 보고됩니다.

## <a name="remarks"></a>설명

C + +에서는 오버 로드 하므로 오버 로드를 호출할 수 있습니다 **fdim** 및 반환 하는 **float** 하 고 **긴** **double** 형식입니다. C 프로그램에서 **fdim** 항상 받아서 반환 된 **double**합니다.

NaN 처리를 제외 하 고이 함수는 동일 `fmax(x - y, 0)`합니다.

## <a name="requirements"></a>요구 사항

|기능|C 헤더|C++ 헤더|
|--------------|--------------|------------------|
|**fdim**하십시오 **fdimf**, **fdiml**|\<math.h>|\<cmath>|

호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="see-also"></a>참고자료

[사전순 함수 참조](crt-alphabetical-function-reference.md)<br/>
[fmax, fmaxf, fmaxl](fmax-fmaxf-fmaxl.md)<br/>
[abs, labs, llabs, _abs64](abs-labs-llabs-abs64.md)<br/>
