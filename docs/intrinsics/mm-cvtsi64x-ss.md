---
title: _mm_cvtsi64x_ss | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- _mm_cvtsi64x_ss
dev_langs:
- C++
helpviewer_keywords:
- cvtsi2ss instruction
- _mm_cvtsi64x_ss intrinsic
ms.assetid: 01e5d321-c18a-46fd-a6f6-324364514e1f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ae300569c4aa04a313f44a23fe988f1de7b826a1
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42543228"
---
# <a name="mmcvtsi64xss"></a>_mm_cvtsi64x_ss
**Microsoft 전용**  
  
 생성 확장 x64 버전 스칼라 단 정밀도 부동 소수점 값으로 변환 하는 64 비트 정수 (`cvtsi2ss`) 명령입니다.  
  
## <a name="syntax"></a>구문  
  
```  
__m128 _mm_cvtsi64x_ss(   
   __m128 a,   
   __int64 b   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [in] `a`  
 `__m128` 네 개의 단 정밀도 부동 소수점 값이 포함 된 구조입니다.  
  
 [in] `b`  
 부동 소수점 값으로 변환 하는 64 비트 정수입니다.  
  
## <a name="return-value"></a>반환 값  
 `__m128` 구조체 인 첫 번째 부동 소수점 값이 변환의 결과입니다. 다른 세 개의 값에서 변경 되지 않고 복사 됩니다 `a`합니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`_mm_cvtsi64x_ss`|X64|  
  
 **헤더 파일** \<intrin.h >  
  
## <a name="remarks"></a>설명  
 합니다 `__m128` 구조는 XMM 레지스터를 나타내며, 값을 허용 하므로 내장 `b` 는 XMM로 이동 될 시스템 메모리에서 등록 합니다.  
  
 이 루틴은 내장 루틴으로만 사용할 수 있습니다.  
  
## <a name="example"></a>예  
  
```  
// _mm_cvtsi64x_ss.cpp  
// processor: x64  
  
#include <intrin.h>  
#include <stdio.h>  
  
#pragma intrinsic(_mm_cvtsi64x_ss)  
  
int main()  
{  
    __m128 a;  
    __int64 b = 54;  
  
    a.m128_f32[0] = 0;  
    a.m128_f32[1] = 0;  
    a.m128_f32[2] = 0;  
    a.m128_f32[3] = 0;  
    a = _mm_cvtsi64x_ss(a, b);  
  
    printf_s( "%lf %lf %lf %lf\n",  
              a.m128_f32[0], a.m128_f32[1],   
              a.m128_f32[2], a.m128_f32[3] );  
}  
```  
  
```Output  
54.000000 0.000000 0.000000 0.000000  
```  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [__m128](../cpp/m128.md)   
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)