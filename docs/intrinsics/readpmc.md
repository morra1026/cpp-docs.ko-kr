---
title: __readpmc
ms.date: 11/04/2016
f1_keywords:
- __readpmc
helpviewer_keywords:
- Read Performance Monitoring Counters instruction
- __readpmc intrinsic
- rdpmc instruction
ms.assetid: 14ed45a6-28b6-4635-8437-a597c04b43d4
ms.openlocfilehash: 059d9344fa329e69666abaca4d73122ab29f8d2a
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326435"
---
# <a name="readpmc"></a>__readpmc

**Microsoft 전용**

생성 된 `rdpmc` 성능 모니터 카운터로 지정 된 된 명령 `counter`입니다.

## <a name="syntax"></a>구문

```
unsigned __int64 __readpmc(
   unsigned long counter
);
```

#### <a name="parameters"></a>매개 변수

*counter*<br/>
[in] 읽기 성능 카운터입니다.

## <a name="return-value"></a>반환 값

지정한 성능 카운터의 값입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__readpmc`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이 내장 함수는 커널 모드 에서만 사용할 수 있습니다 및 루틴은 내장 함수로 사용할 수만 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)