---
title: __writemsr
ms.date: 11/04/2016
f1_keywords:
- __writemsr
helpviewer_keywords:
- Write Model Specific Register instruction
- wrmsr instruction
- __writemsr intrinsic
ms.assetid: 938b1553-51a8-4822-a818-6bed79b0fde5
ms.openlocfilehash: f4af272ccafec9789497d0321c0769c2906f76b7
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51330296"
---
# <a name="writemsr"></a>__writemsr

**Microsoft 전용**

모델 특정 레지스터 쓰기 생성 (`wrmsr`) 명령입니다.

## <a name="syntax"></a>구문

```
void __writemsr(
   unsigned long Register,
   unsigned __int64 Value
);
```

#### <a name="parameters"></a>매개 변수

*등록*<br/>
[in] 모델 특정 레지스터입니다.

*값*<br/>
[in] 쓸 값입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__writemsr`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

커널 모드에서이 함수만 사용할 수 있으며이 루틴은 내장 함수로 사용할 수만 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)