---
title: threadprivate | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- threadprivate
dev_langs:
- C++
helpviewer_keywords:
- threadprivate OpenMP directive
ms.assetid: 3515aaed-6f9d-4d59-85eb-342378bea2d3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0502528a2db47b8db41437fd7017aece1dc67cde
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43217747"
---
# <a name="threadprivate"></a>threadprivate
변수는 스레드에 private 임을 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
#pragma omp threadprivate(var)  
```  
  
## <a name="remarks"></a>설명  
 다음은 각 문자에 대한 설명입니다.  
  
 `var`  
 스레드를 비공개로 하려는 변수의 쉼표로 구분 된 목록입니다. `var` 전역 또는 네임 스페이스-범위 변수 또는 로컬 정적 변수 여야 합니다.  
  
## <a name="remarks"></a>설명  
 `threadprivate` 지시문 없는 OpenMP 절을 지원 합니다.  
  
 자세한 내용은 [2.7.1 threadprivate 지시문](../../../parallel/openmp/2-7-1-threadprivate-directive.md)합니다.  
  
 `threadprivate` 지시문에 기반 합니다 [스레드](../../../cpp/thread.md) `__declspec` 특성;에 대 한 제한 **__declspec (thread)** 적용할 `threadprivate`.  
  
 사용할 수 없습니다 `threadprivate` 를 통해 로드 되는 모든 dll [LoadLibrary](https://msdn.microsoft.com/library/windows/desktop/ms684175)합니다.  여기에 사용 하 여 로드 되는 Dll [/DELAYLOAD (가져오기 로드 지연)](../../../build/reference/delayload-delay-load-import.md)를 사용 하 여 **LoadLibrary**합니다.  
  
 사용할 수 있습니다 `threadprivate` 프로세스를 시작할 때 정적으로 로드 된 dll에서입니다.  
  
 때문에 `threadprivate` 더해서 **__declspec (thread)**, `threadprivate` 변수는 모든 스레드를 병렬 영역에 의해 생성 된 스레드 팀의 일부인 스레드 뿐 아니라 프로세스에서 시작에 존재 합니다.  이 나타날 수 있습니다, 예를 들어 생성자에 대 한 이후를 알아야 할 수 있는 구현 세부 정보를 `threadprivate` 예상 후에 종종 자세한 라는 사용자 정의 형식입니다.  
  
 `threadprivate` destructable 형식의 변수에 해당 소멸자가 호출 하도록 보장 되지 않습니다.  예를 들어:  
  
```  
struct MyType   
{  
    ~MyType();  
};  
  
MyType threaded_var;  
#pragma omp threadprivate(threaded_var)  
int main()   
{  
    #pragma omp parallel  
    {}  
}  
```  
  
 사용자가 병렬 영역을 구성 하는 스레드를 종료 하는 경우에 대 한 제어 하지 않습니다.  프로세스가 종료, 프로세스 종료에 대 한 스레드를 알리지 것입니다 및에 대 한 소멸자가 호출 되지 것입니다 하는 경우 해당 스레드에 있으면 `threaded_var` 끝내는 것을 제외 하 고 모든 스레드에서 (여기, 기본 스레드).  코드의 적절 한 소멸에서 계산 되지 않습니다 있도록 `threadprivate` 변수입니다.  
  
## <a name="example"></a>예제  
 사용 하는 예제에 대 한 `threadprivate`를 참조 하세요 [개인](../../../parallel/openmp/reference/private-openmp.md)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [지시문](../../../parallel/openmp/reference/openmp-directives.md)