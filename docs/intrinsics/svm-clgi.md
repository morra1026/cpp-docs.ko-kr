---
title: __svm_clgi | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __svm_clgi
dev_langs:
- C++
helpviewer_keywords:
- CLGI instruction
- __svm_clgi intrinsic
ms.assetid: 6640f5ab-9472-46f9-a042-e15c4f1ff858
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 54f1a88acef3f3f79a39a8dd68e1beb079f30fec
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42538934"
---
# <a name="svmclgi"></a>__svm_clgi
**Microsoft 전용**  
  
 전역 인터럽트 플래그를 지웁니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __svm_clgi( void );  
```  
  
## <a name="remarks"></a>설명  
 합니다 `__svm_clgi` 함수는 동일 합니다 `CLGI` 컴퓨터 명령입니다. 전역는 인터럽트 플래그를 여부를 결정 마이크로프로세서 무시, 연기, I/O 완료, 하드웨어 온도 경고를 또는 디버그 예외와 같은 이벤트로 인해 인터럽트를 처리 합니다.  
  
 이 함수는 게스트 운영 체제 및 해당 응용 프로그램과 호스트 가상 머신 모니터의 상호 작용을 지원합니다. 자세한 내용은 문서를 검색 "AMD64 아키텍처 프로그래머 수동 볼륨 2: 시스템 프로그래밍"에서 24593, 3.11, 수정 버전 번호를 문서화 합니다 [AMD corporation](http://go.microsoft.com/fwlink/p/?linkid=23746) 사이트입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__svm_clgi`|x86, x64|  
  
 **헤더 파일** \<intrin.h >  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [__svm_stgi](../intrinsics/svm-stgi.md)