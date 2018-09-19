---
title: improper_scheduler_reference 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- improper_scheduler_reference
- CONCRT/concurrency::improper_scheduler_reference
- CONCRT/concurrency::improper_scheduler_reference::improper_scheduler_reference
dev_langs:
- C++
helpviewer_keywords:
- improper_scheduler_reference class
ms.assetid: 434a7512-7796-4255-92a7-f3bf71c6a7a7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: adc6467a66163eeef5916580181005cac1a0a4b6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016939"
---
# <a name="improperschedulerreference-class"></a>improper_scheduler_reference 클래스
이 클래스는 스케줄러에 속하지 않는 컨텍스트에서 종료되는 `Scheduler` 개체에 대해 `Reference` 메서드를 호출하는 경우 발생하는 예외를 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```
class improper_scheduler_reference : public std::exception;
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[improper_scheduler_reference](#ctor)|오버로드됨. `improper_scheduler_reference` 개체를 생성합니다.|  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `exception`  
  
 `improper_scheduler_reference`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  
  
 **네임스페이스:** 동시성  
  
##  <a name="ctor"></a> improper_scheduler_reference 

 `improper_scheduler_reference` 개체를 생성합니다.  
  
```
explicit _CRTIMP improper_scheduler_reference(_In_z_ const char* _Message) throw();

improper_scheduler_reference() throw();
```  
  
### <a name="parameters"></a>매개 변수  
*메시지 (_m)*<br/>
오류 설명 메시지입니다.  
  
## <a name="see-also"></a>참고 항목  
 [Namespace 동시성](concurrency-namespace.md)   
 [Scheduler 클래스](scheduler-class.md)
