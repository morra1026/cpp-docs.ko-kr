---
title: BoolStruct 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 09/21/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::BoolStruct
- internal/Microsoft::WRL::Details::BoolStruct::Member
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Details::BoolStruct structure
- Microsoft::WRL::Details::BoolStruct::Member data member
ms.assetid: 666eae78-e81d-4fb7-a9e4-1ba617d6d4cd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 74a292f2253d29730e8ee9104ea81308081c0496
ms.sourcegitcommit: 1d9bd38cacbc783fccd3884b7b92062161c91c84
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48234270"
---
# <a name="boolstruct-structure"></a>BoolStruct 구조체

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
struct BoolStruct;
```

## <a name="remarks"></a>설명

합니다 `BoolStruct` 구조를 정의 하는지 여부를 `ComPtr` 인터페이스의 개체 수명을 관리 하는 합니다. `BoolStruct` 내부적으로 사용 되는 [BoolType()](../windows/comptr-operator-microsoft-wrl-details-booltype-operator.md) 연산자입니다.

## <a name="members"></a>멤버

### <a name="public-data-members"></a>공용 데이터 멤버

이름                          | 설명
----------------------------- | ------------------------------------------------------------------------------------------------------------------
[Boolstruct:: Member](#member) | 지정 된 [ComPtr](../windows/comptr-class.md) 인지 또는 인터페이스의 개체 수명 관리 되지 합니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`BoolStruct`

## <a name="requirements"></a>요구 사항

**헤더:** internal.h

**Namespace:** Microsoft::WRL::Details

## <a name="member"></a>Boolstruct:: Member

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
int Member;
```

### <a name="remarks"></a>설명

지정 된 [ComPtr](../windows/comptr-class.md) 인지 또는 인터페이스의 개체 수명 관리 되지 합니다.
