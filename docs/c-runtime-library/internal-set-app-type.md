---
title: __set_app_type
ms.date: 11/04/2016
apiname:
- __set_app_type
- _set_app_type
apilocation:
- msvcr90.dll
- msvcr100.dll
- msvcr110.dll
- msvcr80.dll
- msvcrt.dll
- msvcr120.dll
- msvcr110_clr0400.dll
- api-ms-win-crt-runtime-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- __set_app_type
helpviewer_keywords:
- __set_app_type
ms.assetid: f0ac0f4d-70e6-4e96-9e43-eb9d1515490c
ms.openlocfilehash: f42ac1c173637cf85d727adf25ebf9079f4cb37c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50457488"
---
# <a name="setapptype"></a>__set_app_type

현재 응용 프로그램 형식을 설정합니다.

## <a name="syntax"></a>구문

```cpp
void __set_app_type (
   int at
   )
```

#### <a name="parameters"></a>매개 변수

*at*<br/>
응용 프로그램 형식을 나타내는 값입니다. 가능한 값은 다음과 같습니다.

|값|설명|
|-----------|-----------------|
|_UNKNOWN_APP|알 수 없는 응용 프로그램 형식입니다.|
|_CONSOLE_APP|콘솔(명령줄) 응용 프로그램입니다.|
|_GUI_APP|GUI(Windows) 응용 프로그램입니다.|

## <a name="remarks"></a>설명

## <a name="requirements"></a>요구 사항

|루틴에서 반환된 값|필수 헤더|
|-------------|---------------------|
|__set_app_type|internal.h|