---
title: _unlock_file | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- _unlock_file
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
- api-ms-win-crt-filesystem-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _unlock_file
- unlock_file
dev_langs:
- C++
helpviewer_keywords:
- files [C++], unlocking
- unlock_file function
- _unlock_file function
- unlocking files
ms.assetid: cf380a51-6d3a-4f38-bd64-2d4fb57b4369
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 63b0950aaea5520849f9a32b2b08ab138cd8099b
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44107548"
---
# <a name="unlockfile"></a>_unlock_file

다른 프로세스에서 파일에 액세스할 수 있도록 파일의 잠금을 해제합니다.

## <a name="syntax"></a>구문

```C
void _unlock_file(
   FILE* file
);
```

### <a name="parameters"></a>매개 변수

*file*<br/>
파일 핸들입니다.

## <a name="remarks"></a>설명

합니다 **_unlock_file** 함수에서 지정한 파일의 잠금을 해제 *파일*합니다. 파일의 잠금을 해제하면 다른 프로세스에서 파일에 액세스할 수 있습니다. 경우가 아니면이 함수를 호출할 수 해야 **_lock_file** 에서 이전에 호출 된 합니다 *파일* 포인터입니다. 호출 **_unlock_file** 잠겨 있지 않은 파일에서 교착 상태가 발생할 수 있습니다. 관련 예제는 [_lock_file](lock-file.md)을 참조하세요.

## <a name="requirements"></a>요구 사항

|루틴에서 반환된 값|필수 헤더|
|-------------|---------------------|
|**_unlock_file**|\<stdio.h>|

호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="see-also"></a>참고자료

[파일 처리](../../c-runtime-library/file-handling.md)<br/>
[_creat, _wcreat](creat-wcreat.md)<br/>
[_open, _wopen](open-wopen.md)<br/>
[_lock_file](lock-file.md)<br/>
