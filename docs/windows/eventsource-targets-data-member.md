---
title: 'Eventsource:: Targets_ 데이터 멤버 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::EventSource::targets_
dev_langs:
- C++
helpviewer_keywords:
- targets_ data member
ms.assetid: 5d5cee05-3315-4514-bce2-19173c923c7d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: fcdcb759c90009410f76a4b10039a0d976ca0cc4
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42605117"
---
# <a name="eventsourcetargets-data-member"></a>EventSource::targets_ 데이터 멤버

하나 이상의 이벤트 처리기 배열입니다.

## <a name="syntax"></a>구문

```cpp
ComPtr<Details::EventTargetArray> targets_;
```

## <a name="remarks"></a>설명

때 현재 표시 되는 이벤트 **EventSource** 발생 하는 개체, 이벤트 처리기가 호출 됩니다.

## <a name="requirements"></a>요구 사항

**헤더:** event.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목
[EventSource 클래스](../windows/eventsource-class.md)