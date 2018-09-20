---
title: __svm_vmsave | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __svm_vmsave
dev_langs:
- C++
helpviewer_keywords:
- VMSAVE instruction
- __svm_vmsave intrinsic
ms.assetid: 617a60bd-8514-4ba1-8066-bcf4dd481030
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f543fa6c1b1f41040cc6cf13bf2c97cda5b69daf
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46383352"
---
# <a name="svmvmsave"></a>__svm_vmsave

**Microsoft 전용**

지정 된 가상 컴퓨터 제어 블록 (VMCB)의 프로세서 상태 하위 집합을 저장 합니다.

## <a name="syntax"></a>구문

```
void __svm_vmsave(
   size_t VmcbPhysicalAddress
);
```

#### <a name="parameters"></a>매개 변수

|매개 변수|설명|
|---------------|-----------------|
|*VmcbPhysicalAddress*|[in] 실제 주소는 VMCB입니다.|

## <a name="remarks"></a>설명

합니다 `__svm_vmsave` 함수는 동일 합니다 `VMSAVE` 컴퓨터 명령입니다. 이 함수는 게스트 운영 체제 및 해당 응용 프로그램과 호스트 가상 머신 모니터의 상호 작용을 지원합니다. 자세한 내용은 문서를 검색 "AMD64 아키텍처 프로그래머 수동 볼륨 2: 시스템 프로그래밍" 문서 번호 24593, 3.11 이상에서 수정 합니다 [AMD Corporation](https://developer.amd.com/resources/developer-guides-manuals/) 사이트입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__svm_vmsave`|x86, x64|

**헤더 파일** \<intrin.h >

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)<br/>
[__svm_vmrun](../intrinsics/svm-vmrun.md)<br/>
[__svm_vmload](../intrinsics/svm-vmload.md)