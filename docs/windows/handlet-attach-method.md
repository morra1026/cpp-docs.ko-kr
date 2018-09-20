---
title: 'Handlet:: Attach 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleT::Attach
dev_langs:
- C++
helpviewer_keywords:
- Attach method
ms.assetid: a8783a18-bbf6-456c-98a3-e2048a10d79f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5cfb8249d228b5a8e609952e1118bc23a75b9c98
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46426447"
---
# <a name="handletattach-method"></a>HandleT::Attach 메서드

현재 지정된 된 핸들과 연결 **HandleT** 개체입니다.

## <a name="syntax"></a>구문

```cpp
void Attach(
   typename HandleTraits::Type h
);
```

#### <a name="parameters"></a>매개 변수

*h*<br/>
핸들입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HandleT 클래스](../windows/handlet-class.md)