---
title: VerifyInterfaceHelper 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 10/03/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::VerifyInterfaceHelper
- implements/Microsoft::WRL::Details::VerifyInterfaceHelper::Verify
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Details::VerifyInterfaceHelper structure
- Microsoft::WRL::Details::VerifyInterfaceHelper::Verify method
ms.assetid: ea95b641-199a-4fdf-964b-186b40cb3ba7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: b70155566695ade6b6778ade3b4758faebb3ea67
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48788867"
---
# <a name="verifyinterfacehelper-structure"></a>VerifyInterfaceHelper 구조체

Windows Runtime c + + 템플릿 라이브러리 인프라를 지원 하며 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
template <bool isWinRTInterface, typename I>
struct VerifyInterfaceHelper;

template <typename I>
struct VerifyInterfaceHelper<false, I>;
```

### <a name="parameters"></a>매개 변수

*I*<br/>
확인 하는 인터페이스입니다.

*isWinRTInterface*

## <a name="remarks"></a>설명

템플릿 매개 변수로 지정 된 인터페이스에 특정 요구 사항을 충족 하는지 확인 합니다.

## <a name="members"></a>멤버

### <a name="public-methods"></a>Public 메서드

이름                                            | 설명
----------------------------------------------- | ---------------------------------------------------------------------------------------------------
[VerifyInterfaceHelper::Verify 메서드](#verify) | 현재 템플릿 매개 변수로 지정 된 인터페이스에 특정 요구 사항을 충족 하는지 확인 합니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`VerifyInterfaceHelper`

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="verify"></a>Verifyinterfacehelper:: Verify

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
static void Verify();
```

### <a name="remarks"></a>설명

현재 템플릿 매개 변수로 지정 된 인터페이스에 특정 요구 사항을 충족 하는지 확인 합니다.
