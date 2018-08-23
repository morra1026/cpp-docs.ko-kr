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
ms.openlocfilehash: 80af8f463d6cd1af631c6cb37c0239e7a9e85c3f
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42595887"
---
# <a name="hstringhstring-constructor"></a>HString::HString 생성자

새 인스턴스를 초기화 합니다 **HString** 클래스입니다.

## <a name="syntax"></a>구문

```cpp
HString(HSTRING hstr = nullptr) throw();
HString(HString&& other) throw();
```

#### <a name="parameters"></a>매개 변수

*hstr*  
HSTRING 핸들입니다.

*other*  
기존 **HString** 개체입니다.

## <a name="remarks"></a>설명

첫 번째 생성자는 초기화 된 새 **HString** 비어 있는 개체입니다.

두 번째 생성자는 새 **HString** 개체의 기존 값 *다른* 매개 변수를 되지 않으며 합니다 *다른* 매개 변수입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HString 클래스](../windows/hstring-class.md)