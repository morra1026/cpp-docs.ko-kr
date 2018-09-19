---
title: invalid_scheduler_policy_key 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- invalid_scheduler_policy_key
- CONCRT/concurrency::invalid_scheduler_policy_key
- CONCRT/concurrency::invalid_scheduler_policy_key::invalid_scheduler_policy_key
dev_langs:
- C++
helpviewer_keywords:
- invalid_scheduler_policy_key class
ms.assetid: 6a7c42fe-9bc4-4a02-bebb-99fe9ef9817d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1e7dc90ce1ff04d3d02aed13927f137a2b4f7f75
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46113294"
---
# <a name="invalidschedulerpolicykey-class"></a>invalid_scheduler_policy_key 클래스
이 클래스는 잘못되었거나 알 수 없는 키가 `SchedulerPolicy` 개체 생성자에 전달된 경우 또는 `SchedulerPolicy` 개체의 `SetPolicyValue` 메서드에 `SetConcurrencyLimits` 메서드와 같은 기타 방법으로 변경해야 하는 키가 전달된 경우 발생하는 예외를 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```
class invalid_scheduler_policy_key : public std::exception;
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[invalid_scheduler_policy_key](#ctor)|오버로드됨. `invalid_scheduler_policy_key` 개체를 생성합니다.|  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `exception`  
  
 `invalid_scheduler_policy_key`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  
  
 **네임스페이스:** 동시성  
  
##  <a name="ctor"></a> invalid_scheduler_policy_key 

 `invalid_scheduler_policy_key` 개체를 생성합니다.  
  
```
explicit _CRTIMP invalid_scheduler_policy_key(_In_z_ const char* _Message) throw();

invalid_scheduler_policy_key() throw();
```  
  
### <a name="parameters"></a>매개 변수  
*메시지 (_m)*<br/>
오류 설명 메시지입니다.  
  
## <a name="see-also"></a>참고 항목  
 [Namespace 동시성](concurrency-namespace.md)   
 [SchedulerPolicy 클래스](schedulerpolicy-class.md)
