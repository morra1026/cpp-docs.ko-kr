---
title: __readgsbyte, __readgsdword, __readgsqword, __readgsword | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __readgsbyte
- __readgsdword
- __readgsqword
- __readgsword
dev_langs:
- C++
helpviewer_keywords:
- __readgsword intrinsic
- __readgsdword intrinsic
- __readgsqword intrinsic
- __readgsbyte intrinsic
ms.assetid: f822632d-854c-4558-a71b-cdfc3eea2236
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8afe4d646e77e87c1c679d8b7e3bd09679c7b16d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46414552"
---
# <a name="readgsbyte-readgsdword-readgsqword-readgsword"></a>__readgsbyte, __readgsdword, __readgsqword, __readgsword

**Microsoft 전용**

GS 세그먼트의 시작을 기준으로 오프셋으로 지정 된 위치에서 메모리를 읽습니다.

## <a name="syntax"></a>구문

```
unsigned char __readgsbyte( 
   unsigned long Offset 
);
unsigned short __readgsword( 
   unsigned long Offset 
);
unsigned long __readgsdword( 
   unsigned long Offset
);
unsigned __int64 __readgsqword( 
   unsigned long Offset 
);
```

#### <a name="parameters"></a>매개 변수

*오프셋*<br/>
[in] 시작 부분 으로부터의 오프셋 `GS` 에서 읽을 수 있습니다.

## <a name="return-value"></a>반환 값

메모리 내용의 바이트, word, 2 배 워드를 또는 쿼드 워드 (호출 함수의 이름으로 표시) 하는 대로 위치 `GS:[Offset]`합니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__readgsbyte`|X64|
|`__readgsdword`|X64|
|`__readgsqword`|X64|
|`__readgsword`|X64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이러한 내장 함수 에서만 커널 모드에서 사용할 수 있으며 루틴은 내장 함수로 사용할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[__writegsbyte, \__writegsdword, \__writegsqword, \__writegsword](../intrinsics/writegsbyte-writegsdword-writegsqword-writegsword.md)<br/>
[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)