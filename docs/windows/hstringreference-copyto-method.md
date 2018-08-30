---
title: 'Hstringreference:: Copyto 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
ms.assetid: 179d9b14-1ced-4b16-b297-19ca1e92a462
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 0299f469f9cd2757c72e05a8717171ec32aa2c6c
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43198526"
---
# <a name="hstringreferencecopyto-method"></a>HStringReference::CopyTo 메서드

현재 복사 **HStringReference** 개체를 HSTRING 개체로 합니다.

## <a name="syntax"></a>구문

```cpp
HRESULT CopyTo(
   _Out_ HSTRING *str
   ) const throw();
```

### <a name="parameters"></a>매개 변수

*str*  
복사본을 받는 HSTRING입니다.

## <a name="remarks"></a>설명

이 메서드를 호출 합니다 [WindowsDuplicateString](https://msdn.microsoft.com/library/br224634.aspx) 함수입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HStringReference 클래스](../windows/hstringreference-class.md)