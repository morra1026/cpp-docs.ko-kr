---
title: improper_scheduler_attach 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- improper_scheduler_attach
- CONCRT/concurrency::improper_scheduler_attach
- CONCRT/concurrency::improper_scheduler_attach::improper_scheduler_attach
dev_langs:
- C++
helpviewer_keywords:
- improper_scheduler_attach class
ms.assetid: 5a76da0a-091b-4748-8f62-b3a28f674f9e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9b51c3d800195f265a0ed0a717c7e8f318434306
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46412877"
---
# <a name="improperschedulerattach-class"></a>improper_scheduler_attach 클래스

이 클래스는 동일한 컨텍스트에 이미 연결된 `Scheduler` 개체에 대해 `Attach` 메서드를 호출하는 경우 발생하는 예외를 설명합니다.

## <a name="syntax"></a>구문

```
class improper_scheduler_attach : public std::exception;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[improper_scheduler_attach](#ctor)|오버로드됨. `improper_scheduler_attach` 개체를 생성합니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`exception`

`improper_scheduler_attach`

## <a name="requirements"></a>요구 사항

**헤더:** concrt.h

**네임스페이스:** 동시성

##  <a name="ctor"></a> improper_scheduler_attach

`improper_scheduler_attach` 개체를 생성합니다.

```
explicit _CRTIMP improper_scheduler_attach(_In_z_ const char* _Message) throw();

improper_scheduler_attach() throw();
```

### <a name="parameters"></a>매개 변수

*메시지 (_m)*<br/>
오류 설명 메시지입니다.

## <a name="see-also"></a>참고 항목

[concurrency 네임스페이스](concurrency-namespace.md)<br/>
[Scheduler 클래스](scheduler-class.md)
