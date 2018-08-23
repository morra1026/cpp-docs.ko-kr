---
title: 'Asyncbase:: Getoncomplete 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncBase::GetOnComplete
dev_langs:
- C++
helpviewer_keywords:
- GetOnComplete method
ms.assetid: f06ae02d-9a88-41d2-b749-bdc1a7ff8748
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: eab2a577d0c7b31f833a8dcc0208f9939b729ad9
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42607471"
---
# <a name="asyncbasegetoncomplete-method"></a>AsyncBase::GetOnComplete 메서드

지정된 된 변수를 현재 완료 이벤트 처리기의 주소를 복사합니다.

## <a name="syntax"></a>구문

```cpp
STDMETHOD(
   GetOnComplete
)(TComplete** completeHandler);
```

### <a name="parameters"></a>매개 변수

*completeHandler*  
현재 완료 이벤트 처리기의 주소를 저장 된 위치입니다.

## <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** async.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[AsyncBase 클래스](../windows/asyncbase-class.md)