---
title: out_of_memory 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-amp
ms.topic: reference
f1_keywords:
- out_of_memory
- AMPRT/out_of_memory
- AMPRT/Concurrency::out_of_memory::out_of_memory
dev_langs:
- C++
helpviewer_keywords:
- out_of_memory class
ms.assetid: 3aa7e682-8f13-4ae6-9188-31fb423956e4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b57e27647f61b551f8ea5c2770290e1ae9627014
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070927"
---
# <a name="outofmemory-class"></a>out_of_memory 클래스
장치 또는 시스템 메모리 부족으로 인해 메서드가 실패할 때 throw 되는 예외입니다.  
  
## <a name="syntax"></a>구문  
  
```  
class out_of_memory : public runtime_exception;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[out_of_memory 생성자](#ctor)|`out_of_memory` 클래스의 새 인스턴스를 초기화합니다.|  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `exception`  
  
 `runtime_exception`  
  
 `out_of_memory`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** amprt.h  
  
 **네임스페이스:** 동시성  
## <a name="ctor"></a> out_of_memory 

 클래스의 새 인스턴스를 초기화합니다.  
  
### <a name="syntax"></a>구문  
  
```  
explicit out_of_memory(  
    const char * _Message ) throw();  
  
out_of_memory () throw();  
```  
  
### <a name="parameters"></a>매개 변수  
*메시지 (_m)*<br/>
오류에 대한 설명입니다.  
  
### <a name="return-value"></a>반환 값  
 `out_of_memory` 클래스의 새 인스턴스입니다.  
  
  
## <a name="see-also"></a>참고 항목  
 [Concurrency 네임스페이스(C++ AMP)](concurrency-namespace-cpp-amp.md)
