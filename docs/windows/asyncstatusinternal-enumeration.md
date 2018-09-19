---
title: AsyncStatusInternal 열거형 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::Details::AsyncStatusInternal
dev_langs:
- C++
helpviewer_keywords:
- AsyncStatusInternal enumeration
ms.assetid: b783923f-3f1c-4487-9384-be572cbc62d7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 4c7751929a55993876034bb3c1918b82193681fc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016886"
---
# <a name="asyncstatusinternal-enumeration"></a>AsyncStatusInternal 열거형

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
enum AsyncStatusInternal;
```

## <a name="remarks"></a>설명

비동기 작업의 상태 내부 열거형 사이 매핑을 지정 및 `Windows::Foundation::AsyncStatus` 열거형입니다.

## <a name="members"></a>멤버

`_Created`<br/>
`::Windows::Foundation::AsyncStatus::Created`와 같습니다.

`_Started`<br/>
`::Windows::Foundation::AsyncStatus::Started`와 같습니다.

`_Completed`<br/>
`::Windows::Foundation::AsyncStatus::Completed`와 같습니다.

`_Cancelled`<br/>
`::Windows::Foundation::AsyncStatus::Cancelled`와 같습니다.

`_Error`<br/>
`::Windows::Foundation::AsyncStatus::Error`와 같습니다.

## <a name="requirements"></a>요구 사항

**헤더:** async.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)