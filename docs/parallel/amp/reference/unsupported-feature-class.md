---
title: unsupported_feature 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-amp
ms.topic: reference
f1_keywords:
- unsupported_feature
- AMPRT/unsupported_feature
- AMPRT/Concurrency::unsupported_feature
dev_langs:
- C++
helpviewer_keywords:
- unsupported_feature class
ms.assetid: 6b1ab917-df13-48c7-9648-7cb2465a0ff5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4ed33df07ed6fe9f99f5e9a135e3286672e7a013
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46393570"
---
# <a name="unsupportedfeature-class"></a>unsupported_feature 클래스

지원 되지 않는 기능을 사용 하는 경우 throw 되는 예외입니다.

## <a name="syntax"></a>구문

```
class unsupported_feature : public runtime_exception;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[unsupported_feature 생성자](#ctor)|새 인스턴스를 생성 합니다 `unsupported_feature` 예외입니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`exception`

`runtime_exception`

`unsupported_feature`

## <a name="unsupported_feature__ctor"></a> unsupported_feature

  Unsupported_feature 예외의 새 인스턴스를 생성합니다.

### <a name="syntax"></a>구문

```
explicit unsupported_feature(
    const char * _Message ) throw();

unsupported_feature() throw();
```

### <a name="parameters"></a>매개 변수

*메시지 (_m)*<br/>
오류에 대한 설명입니다.

### <a name="return-value"></a>반환 값

`unsupported_feature` 개체

## <a name="requirements"></a>요구 사항

**헤더:** amprt.h

**네임스페이스:** 동시성

## <a name="see-also"></a>참고 항목

[Concurrency 네임스페이스(C++ AMP)](concurrency-namespace-cpp-amp.md)
