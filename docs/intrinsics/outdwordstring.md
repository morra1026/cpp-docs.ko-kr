---
title: __outdwordstring
ms.date: 11/04/2016
f1_keywords:
- __outdwordstring
helpviewer_keywords:
- outsd instruction
- __outdwordstring intrinsic
- rep outsd instruction
ms.assetid: 55b31a65-aab7-4b5c-b61d-d9e2fb0c497a
ms.openlocfilehash: 5579258c813850cdb8f29758bb4bd5d87270467f
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51330283"
---
# <a name="outdwordstring"></a>__outdwordstring

**Microsoft 전용**

생성 된 `rep outsd` 명령을 보냅니다 `Count` 에서 시작 하는 2 배 워드 `Buffer` 로 지정 된 I/O 포트를 찾기 `Port`.

## <a name="syntax"></a>구문

```
void __outdwordstring(
   unsigned short Port,
   unsigned long* Buffer,
   unsigned long Count
);
```

#### <a name="parameters"></a>매개 변수

*포트*<br/>
[in] 데이터를 보낼 포트입니다.

*Buffer*<br/>
[in] 지정된 된 포트에 보내도록 데이터에 대 한 포인터입니다.

*개수*<br/>
[in] 보낼 2 배 워드 횟수입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__outdwordstring`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이 루틴은 내장 루틴으로만 사용할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)