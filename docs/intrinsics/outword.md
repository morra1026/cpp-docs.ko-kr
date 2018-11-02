---
title: __outword
ms.date: 11/04/2016
f1_keywords:
- __outword
helpviewer_keywords:
- __outword intrinsic
- out instruction
ms.assetid: 995f8834-0f50-4b4f-a7a2-af0e7c371cda
ms.openlocfilehash: e5a6274fef9d9e9e4a168b9849ab0021c32a4716
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50626189"
---
# <a name="outword"></a>__outword

**Microsoft 전용**

생성 된 `out` 단어를 전송 하는 명령 `Data` 로 지정 된 I/O 포트를 찾기 `Port`합니다.

## <a name="syntax"></a>구문

```
void __outword( 
   unsigned short Port, 
   unsigned short Data 
);
```

#### <a name="parameters"></a>매개 변수

*포트*<br/>
[in] 데이터를 보낼 포트입니다.

*Data*<br/>
[in] 데이터 전송입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__outword`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이 루틴은 내장 루틴으로만 사용할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)