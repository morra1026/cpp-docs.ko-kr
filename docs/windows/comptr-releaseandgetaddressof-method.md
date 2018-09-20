---
title: 'Comptr:: Releaseandgetaddressof 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::ComPtr::ReleaseAndGetAddressOf
dev_langs:
- C++
helpviewer_keywords:
- ReleaseAndGetAddressOf method
ms.assetid: 3751dcb4-d50e-432c-89e4-e736be34d434
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 7f4aee13808fd55c42319aab90c13af7922ed9d2
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46394841"
---
# <a name="comptrreleaseandgetaddressof-method"></a>ComPtr::ReleaseAndGetAddressOf 메서드

와 연결 된 인터페이스를 해제 **ComPtr** 다음의 주소를 검색 합니다 [ptr_](../windows/comptr-ptr-data-member.md) 출시 된 인터페이스에 대 한 포인터를 포함 하는 데이터 멤버입니다.

## <a name="syntax"></a>구문

```cpp
T** ReleaseAndGetAddressOf();
```

## <a name="return-value"></a>반환 값

주소를 [ptr_](../windows/comptr-ptr-data-member.md) 이 데이터 멤버 **ComPtr**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[ComPtr 클래스](../windows/comptr-class.md)<br/>
[ComPtr::ptr_ 데이터 멤버](../windows/comptr-ptr-data-member.md)