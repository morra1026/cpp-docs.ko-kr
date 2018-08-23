---
title: ActivateInstance 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Windows::Foundation::ActivateInstance
- client/ABI::Windows::Foundation::ActivateInstance
dev_langs:
- C++
helpviewer_keywords:
- ActivateInstance function
ms.assetid: 8cfd1dd9-5fda-4cc2-acf8-d40e783b3875
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: c2ac6d8722bcdfed06ae97508b0ca7e5bb8ea00a
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42601454"
---
# <a name="activateinstance-function"></a>ActivateInstance 함수

등록 하 고 ID가 지정 된 클래스에 정의 된 지정 된 형식의 인스턴스를 검색 합니다.

## <a name="syntax"></a>구문

```cpp
template<typename T>
inline HRESULT ActivateInstance(
   _In_ HSTRING activatableClassId,
   _Out_ Microsoft::WRL::Details::ComPtrRef<T> instance
);
```

### <a name="parameters"></a>매개 변수

*T*  
활성화 하는 형식입니다.

*activatableClassId*  
매개 변수를 정의 하는 클래스 ID의 이름을 *T*합니다.

*인스턴스*  
이 작업이 완료 될 때, 인스턴스에 대 한 참조 *T*합니다.

## <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않은 경우 오류의 원인을 나타내는 HRESULT 오류가 발생 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**Namespace:** windows:: foundation

## <a name="see-also"></a>참고 항목

[Windows::Foundation 네임스페이스](../windows/windows-foundation-namespace.md)