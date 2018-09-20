---
title: 'Eventtargetarray:: Eventtargetarray 생성자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::EventTargetArray::EventTargetArray
dev_langs:
- C++
helpviewer_keywords:
- EventTargetArray, constructor
ms.assetid: 6c6d3737-3cd3-4515-a8f6-d27901bb8ed2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: dc59b9c93cebb622f40881d961709079abcd9166
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46388632"
---
# <a name="eventtargetarrayeventtargetarray-constructor"></a>EventTargetArray::EventTargetArray 생성자

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
EventTargetArray(
   _Out_ HRESULT* hr,
   size_t items
);
```

### <a name="parameters"></a>매개 변수

*hr*<br/>
이 생성자 작업을 수행한 후 매개 변수 *hr* 배열 할당 성공 또는 실패 여부를 나타냅니다. 다음 표에서 대 한 가능한 값 *hr*합니다.

S_ok이 고, 작업에 성공 했습니다.

배열에 대 한 e_outofmemory가 메모리를 할당할 수 없습니다.

S_FALSE 매개 변수 *항목* 0 보다 작거나 같음.

*항목*<br/>
할당할 배열의 요소 수입니다.

## <a name="remarks"></a>설명

새 인스턴스를 초기화 합니다 **EventTargetArray** 클래스입니다.

**EventTargetArray** 이벤트 처리기의 배열을 유지 하는 데 사용 되는 `EventSource` 개체입니다.

## <a name="requirements"></a>요구 사항

**헤더:** event.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[EventTargetArray 클래스](../windows/eventtargetarray-class.md)<br/>
[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)