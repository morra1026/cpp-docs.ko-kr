---
title: scheduler_ptr 구조체
ms.date: 11/04/2016
f1_keywords:
- scheduler_ptr
- PPLINTERFACE/concurrency::scheduler_ptr
- PPLINTERFACE/concurrency::scheduler_ptr::scheduler_ptr::scheduler_ptr
- PPLINTERFACE/concurrency::scheduler_ptr::scheduler_ptr::get
- PPLINTERFACE/concurrency::scheduler_ptr::scheduler_ptr::operator bool
ms.assetid: e88c84af-c306-476d-aef1-f42a0fa0a80f
ms.openlocfilehash: 0da45fa18d12b3f1c93df6b8c8736ed1bfb58ade
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2018
ms.locfileid: "51525006"
---
# <a name="schedulerptr-structure"></a>scheduler_ptr 구조체

스케줄러에 대한 포인터를 나타냅니다. 이 클래스는 공유 수명 사양의 원시 포인터를 사용 하 여 shared_ptr 또는 일반 참조를 사용 하 여 있도록 존재 합니다.

## <a name="syntax"></a>구문

```
struct scheduler_ptr;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[scheduler_ptr::scheduler_ptr](#ctor)|오버로드됨. shared_ptr에서 스케줄러에 대한 스케줄러 포인터를 만듭니다.|

### <a name="public-methods"></a>Public 메서드

|이름|설명|
|----------|-----------------|
|[scheduler_ptr::get](#get)|스케줄러에 대한 원시 포인터를 반환합니다.|

### <a name="public-operators"></a>Public 연산자

|이름|설명|
|----------|-----------------|
|[scheduler_ptr::operator bool](#operator_bool)|스케줄러 포인터가 null이 아닌지 여부를 테스트합니다.|
|[scheduler_ptr::operator-&gt;](#operator_ptr)|포인터처럼 작동합니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`scheduler_ptr`

## <a name="requirements"></a>요구 사항

**헤더:** pplinterface.h

**네임스페이스:** 동시성

##  <a name="get"></a>  scheduler_ptr:: get 메서드

스케줄러에 원시 포인터를 반환합니다.

```
scheduler_interface* get() const;
```

### <a name="return-value"></a>반환 값

##  <a name="operator_bool"></a>  scheduler_ptr::operator bool

스케줄러 포인터가 null 인지 테스트 합니다.

```
operator bool() const;
```

##  <a name="operator_ptr"></a>  scheduler_ptr:: operator-&gt;

에 대 한 포인터 처럼 동작합니다.

```
scheduler_interface* operator->() const;
```

### <a name="return-value"></a>반환 값

##  <a name="ctor"></a>  scheduler_ptr:: scheduler_ptr 생성자

Shared_ptr에서 스케줄러에 대 한 스케줄러 포인터를 만듭니다.

```
explicit scheduler_ptr(std::shared_ptr<scheduler_interface> scheduler);
explicit scheduler_ptr(_In_opt_ scheduler_interface* pScheduler);
```

### <a name="parameters"></a>매개 변수

*scheduler*<br/>
변환할 스케줄러입니다.

*pScheduler*<br/>
변환할 스케줄러 포인터입니다.

## <a name="see-also"></a>참고 항목

[concurrency 네임스페이스](concurrency-namespace.md)
