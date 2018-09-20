---
title: 'Handlenulltraits:: Close 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits::Close
dev_langs:
- C++
helpviewer_keywords:
- Close method
ms.assetid: 6fb2fa0d-df20-45dc-856f-f78497f8bdf9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 1041fc03a565592784131102a48ffe2ded0e159c
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46430645"
---
# <a name="handlenulltraitsclose-method"></a>HANDLENullTraits::Close 메서드

지정된 된 핸들을 닫습니다.

## <a name="syntax"></a>구문

```cpp
inline static bool Close(
   _In_ Type h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
핸들 닫기입니다.

## <a name="return-value"></a>반환 값

**true** 경우 처리할 *h* 이 고, 그렇지 않으면 닫은 **false**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="see-also"></a>참고 항목

[HANDLENullTraits 구조체](../windows/handlenulltraits-structure.md)