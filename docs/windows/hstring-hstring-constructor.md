---
title: 'Hstring:: Hstring 생성자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HString::HString
dev_langs:
- C++
ms.assetid: 6da12785-ed01-4720-a004-667db60298f1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 59ec7c1635b825cc300e28e5c02e2a3864a6c123
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46442255"
---
# <a name="hstringhstring-constructor"></a>HString::HString 생성자

새 인스턴스를 초기화 합니다 **HString** 클래스입니다.

## <a name="syntax"></a>구문

```cpp
HString(HSTRING hstr = nullptr) throw();
HString(HString&& other) throw();
```

#### <a name="parameters"></a>매개 변수

*hstr*<br/>
HSTRING 핸들입니다.

*other*<br/>
기존 **HString** 개체입니다.

## <a name="remarks"></a>설명

첫 번째 생성자는 초기화 된 새 **HString** 비어 있는 개체입니다.

두 번째 생성자는 새 **HString** 개체의 기존 값 *다른* 매개 변수를 되지 않으며 합니다 *다른* 매개 변수입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HString 클래스](../windows/hstring-class.md)