---
title: __readfsbyte, __readfsdword, __readfsqword, __readfsword | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __readfsword
- __readfsdword
- __readfsbyte
- __readfsqword
dev_langs:
- C++
helpviewer_keywords:
- __readfsword intrinsic
- readfsword intrinsic
- __readfsdword intrinsic
- readfsbyte intrinsic
- __readfsbyte intrinsic
- readfsdword intrinsic
- readfsqword intrinsic
- __readfsqword intrinsic
ms.assetid: f6ee7203-4179-402c-a464-0746c84ce6ac
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 102eecb30c1ed857fdbb9a7294d95db9961a1765
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46392049"
---
# <a name="readfsbyte-readfsdword-readfsqword-readfsword"></a>__readfsbyte, __readfsdword, __readfsqword, __readfsword

**Microsoft 전용**

FS 세그먼트의 시작을 기준으로 오프셋으로 지정 된 위치에서 메모리를 읽습니다.

## <a name="syntax"></a>구문

```
unsigned char __readfsbyte( 
   unsigned long Offset 
);
unsigned short __readfsword( 
   unsigned long Offset 
);
unsigned long __readfsdword( 
   unsigned long Offset
);
unsigned __int64 __readfsqword( 
   unsigned long Offset 
);
```

#### <a name="parameters"></a>매개 변수

*오프셋*<br/>
[in] 시작 부분 으로부터의 오프셋 `FS` 에서 읽을 수 있습니다.

## <a name="return-value"></a>반환 값

메모리 내용의 바이트, 단어, 워드, 또는 (호출 함수의 이름으로 표시) 하는 대로 쿼드 워드 위치의 `FS:[Offset]`합니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__readfsbyte`|x86|
|`__readfsdword`|x86|
|`__readfsqword`|x86|
|`__readfsword`|x86|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이러한 루틴은 내장 함수로 사용할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[__writefsbyte, \__writefsdword, \__writefsqword, \__writefsword](../intrinsics/writefsbyte-writefsdword-writefsqword-writefsword.md)<br/>
[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)