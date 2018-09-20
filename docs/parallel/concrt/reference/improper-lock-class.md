---
title: improper_lock 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- improper_lock
- CONCRT/concurrency::improper_lock
- CONCRT/concurrency::improper_lock::improper_lock
dev_langs:
- C++
helpviewer_keywords:
- improper_lock class
ms.assetid: 8f494942-7748-4a2a-8de2-23414bfe6346
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 655776543a0c368bf5d13719d10b507c941a0fa9
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46404698"
---
# <a name="improperlock-class"></a>improper_lock 클래스

이 클래스는 부적절하게 잠금을 얻은 경우 발생하는 예외를 설명합니다.

## <a name="syntax"></a>구문

```
class improper_lock : public std::exception;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[improper_lock](#ctor)|오버로드됨. `improper_lock exception`를 생성합니다.|

## <a name="remarks"></a>설명

일반적으로 동일한 컨텍스트에서 재진입 잠금을 재귀적으로 획득 하려고 시도 하는 경우이 예외가 throw 됩니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`exception`

`improper_lock`

## <a name="requirements"></a>요구 사항

**헤더:** concrt.h

**네임스페이스:** 동시성

##  <a name="ctor"></a> improper_lock

`improper_lock exception`를 생성합니다.

```
explicit _CRTIMP improper_lock(_In_z_ const char* _Message) throw();

improper_lock() throw();
```

### <a name="parameters"></a>매개 변수

*메시지 (_m)*<br/>
오류 설명 메시지입니다.

## <a name="see-also"></a>참고 항목

[concurrency 네임스페이스](concurrency-namespace.md)<br/>
[critical_section 클래스](critical-section-class.md)<br/>
[reader_writer_lock 클래스](reader-writer-lock-class.md)
