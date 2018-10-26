---
title: SafeIntException 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 10/22/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- SafeIntException Class
- SafeIntException
- SafeIntException.SafeIntException
- SafeIntException::SafeIntException
dev_langs:
- C++
helpviewer_keywords:
- SafeIntException class
- SafeIntException, constructor
ms.assetid: 88bef958-1f48-4d55-ad4f-d1f9581a293a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2a1890bc20c0737007075656dcbefa20ad81a9bf
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50068062"
---
# <a name="safeintexception-class"></a>SafeIntException 클래스

합니다 `SafeInt` 클래스는 `SafeIntException` 수학 작업을 완료할 수 없습니다는 이유를 확인 하려면.

> [!NOTE]
> 이 라이브러리의 최신 버전에 위치한 [ https://github.com/dcleblanc/SafeInt ](https://github.com/dcleblanc/SafeInt)합니다.

## <a name="syntax"></a>구문

```cpp
class SafeIntException;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

이름                                                    | 설명
------------------------------------------------------- | ------------------------------------
[SafeIntException::SafeIntException](#safeintexception) | `SafeIntException` 개체를 만듭니다.

## <a name="remarks"></a>설명

합니다 [SafeInt 클래스](../windows/safeint-class.md) 사용 하는 유일한 클래스는 `SafeIntException` 클래스입니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`SafeIntException`

## <a name="requirements"></a>요구 사항

**헤더:** safeint.h

**Namespace:** msl:: utilities

## <a name="safeintexception"></a>Safeintexception:: Safeintexception

`SafeIntException` 개체를 만듭니다.

```cpp
SafeIntException();

SafeIntException(
   SafeIntError code
);
```

### <a name="parameters"></a>매개 변수

*코드*<br/>
[in] 발생 한 오류를 설명 하는 열거형된 데이터 값입니다.

### <a name="remarks"></a>설명

가능한 값에 대 한 *코드* Safeint.h 파일에 정의 됩니다. 편의 위해 가능한 값도 여기에 나와 있습니다.

- `SafeIntNoError`
- `SafeIntArithmeticOverflow`
- `SafeIntDivideByZero`
