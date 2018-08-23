---
title: 'Asyncbase:: Trytransitiontocompleted 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncBase::TryTransitionToCompleted
dev_langs:
- C++
helpviewer_keywords:
- TryTransitionToCompleted method
ms.assetid: 8d038e0a-47ec-4cfc-8aeb-6821282df67a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 3f1f6e27c7797a8995044bdcf9ebd9425a6f6ea3
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42604165"
---
# <a name="asyncbasetrytransitiontocompleted-method"></a>AsyncBase::TryTransitionToCompleted 메서드

현재 비동기 작업이 완료 되었는지 여부를 나타냅니다.

## <a name="syntax"></a>구문

```cpp
bool TryTransitionToCompleted(
   void
);
```

## <a name="return-value"></a>반환 값

**true 이면** 비동기 작업이 완료 되었으면;이 고, 그렇지 **false**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** async.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[AsyncBase 클래스](../windows/asyncbase-class.md)