---
title: 'Eventsource:: Targetspointerlock_ 데이터 멤버 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::EventSource::targetsPointerLock_
dev_langs:
- C++
helpviewer_keywords:
- targetsPointerLock_ data member
ms.assetid: 8f08409f-5262-4be7-9cf1-2ed15f19684a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 45c85502b7d0768f5fa3e275393a4071fd8649e4
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42598867"
---
# <a name="eventsourcetargetspointerlock-data-member"></a>EventSource::targetsPointerLock_ 데이터 멤버

이 대 한 이벤트 처리기는 동안에 내부 데이터 멤버에 대 한 액세스를 동기화 **EventSource** 추가, 제거 또는 호출 합니다.

## <a name="syntax"></a>구문

```cpp
Wrappers::SRWLock targetsPointerLock_;
```

## <a name="requirements"></a>요구 사항

**헤더:** event.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목
[EventSource 클래스](../windows/eventsource-class.md)