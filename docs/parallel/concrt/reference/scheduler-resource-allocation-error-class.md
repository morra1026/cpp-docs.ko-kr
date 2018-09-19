---
title: scheduler_resource_allocation_error 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- scheduler_resource_allocation_error
- CONCRT/concurrency::scheduler_resource_allocation_error
- CONCRT/concurrency::scheduler_resource_allocation_error::scheduler_resource_allocation_error
- CONCRT/concurrency::scheduler_resource_allocation_error::get_error_code
dev_langs:
- C++
helpviewer_keywords:
- scheduler_resource_allocation_error class
ms.assetid: 8b40449a-7abb-4d0a-bb85-c0e9a495ae97
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9ede37cec7b654c2d5ead32f117e4fe76f28fa60
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46101698"
---
# <a name="schedulerresourceallocationerror-class"></a>scheduler_resource_allocation_error 클래스
이 클래스는 동시성 런타임에서 중요한 리소스를 얻지 못해 발생하는 예외를 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```
class scheduler_resource_allocation_error : public std::exception;
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[scheduler_resource_allocation_error](#ctor)|오버로드됨. `scheduler_resource_allocation_error` 개체를 생성합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[get_error_code](#get_error_code)|예외를 발생 시킨 오류 코드를 반환 합니다.|  
  
## <a name="remarks"></a>설명  
 이 예외는 일반적으로 동시성 런타임 내에서 운영 체제 호출이 실패할 때 throw 됩니다. 일반적으로 Win32 메서드 `GetLastError`에 대한 호출에서 반환되는 오류 코드는 `HRESULT` 형식의 값으로 변환되므로 `get_error_code` 메서드를 사용하여 검색할 수 있습니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `exception`  
  
 `scheduler_resource_allocation_error`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** concrt.h  
  
 **네임스페이스:** 동시성  
  
##  <a name="get_error_code"></a> get_error_code 

 예외를 발생 시킨 오류 코드를 반환 합니다.  
  
```
HRESULT get_error_code() const throw();
```  
  
### <a name="return-value"></a>반환 값  
 `HRESULT` 예외를 발생 시킨 오류 값입니다.  
  
##  <a name="ctor"></a> scheduler_resource_allocation_error 

 `scheduler_resource_allocation_error` 개체를 생성합니다.  
  
```
scheduler_resource_allocation_error(
    _In_z_ const char* _Message,
    HRESULT _Hresult) throw();

explicit _CRTIMP scheduler_resource_allocation_error(
    HRESULT _Hresult) throw();
```  
  
### <a name="parameters"></a>매개 변수  
*메시지 (_m)*<br/>
오류 설명 메시지입니다.  
  
*_Hresult*<br/>
`HRESULT` 예외를 발생 시킨 오류 값입니다.  
  
## <a name="see-also"></a>참고 항목  
 [concurrency 네임스페이스](concurrency-namespace.md)
