---
title: invalid_scheduler_policy_value 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- concrt/concurrency::invalid_scheduler_policy_value
dev_langs:
- C++
helpviewer_keywords:
- invalid_scheduler_policy_value class
ms.assetid: 8c533e3f-2774-4192-8616-b2313b859bf7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0bc8f0d34a49cf8392fec13f956f4577a67248e3
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46402748"
---
# <a name="invalidschedulerpolicyvalue-class"></a>invalid_scheduler_policy_value 클래스

이 클래스는 `SchedulerPolicy` 개체의 정책 키가 해당 키에 잘못된 값으로 설정된 경우 발생하는 예외를 설명합니다.

## <a name="syntax"></a>구문

```
class invalid_scheduler_policy_value : public std::exception;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[invalid_scheduler_policy_value](invalid-scheduler-policy-thread-specification-class.md#ctor|오버로드됨. `invalid_scheduler_policy_value` 개체를 생성합니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`exception`

`invalid_scheduler_policy_value`

## <a name="requirements"></a>요구 사항

**헤더:** concrt.h

**네임스페이스:** 동시성

##  <a name="ctor"></a> invalid_scheduler_policy_value

`invalid_scheduler_policy_value` 개체를 생성합니다.

```
explicit _CRTIMP invalid_scheduler_policy_value(_In_z_ const char* _Message) throw();

invalid_scheduler_policy_value() throw();
```

### <a name="parameters"></a>매개 변수

*메시지 (_m)*<br/>
오류 설명 메시지입니다.

## <a name="see-also"></a>참고 항목

[concurrency 네임스페이스](concurrency-namespace.md)<br/>
[SchedulerPolicy 클래스](schedulerpolicy-class.md)
