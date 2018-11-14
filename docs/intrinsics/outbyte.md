---
title: __outbyte
ms.date: 11/04/2016
f1_keywords:
- __outbyte
helpviewer_keywords:
- out instruction
- __outbyte intrinsic
ms.assetid: c4cd1a34-8a02-4e37-993d-3201bc17901a
ms.openlocfilehash: fa17e4859e861a9be46b4ad32b7ad090f6c3dbc6
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326552"
---
# <a name="outbyte"></a>__outbyte

**Microsoft 전용**

생성 된 `out` 명령으로 지정 된 1 바이트를 전송 하는 `Data` 로 지정 된 I/O 포트를 찾기 `Port`합니다.

## <a name="syntax"></a>구문

```
void __outbyte(
   unsigned short Port,
   unsigned char Data
);
```

#### <a name="parameters"></a>매개 변수

*포트*<br/>
[in] 데이터를 보낼 포트입니다.

*Data*<br/>
[in] 지정된 된 포트에 보내도록 바이트입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__outbyte`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이 루틴은 내장 루틴으로만 사용할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)