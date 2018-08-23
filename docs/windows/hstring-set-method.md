---
title: 'Hstring:: Set 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HString::Set
dev_langs:
- C++
ms.assetid: c9b3d613-95c4-48b0-999d-f5baf0804faf
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 6eb2261ab973245c78ec8f5e0269663e5181a0ab
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42590043"
---
# <a name="hstringset-method"></a>HString::Set 메서드

현재 값을 설정 **HString** 지정된 된 와이드 문자 문자열에는 개체 또는 **HString** 매개 변수입니다.

## <a name="syntax"></a>구문

```cpp
HRESULT Set(
          const wchar_t* str) throw();
HRESULT Set(
          const wchar_t* str,
          unsigned int len
           ) throw();
HRESULT Set(
          const HSTRING& hstr
           ) throw();
```

### <a name="parameters"></a>매개 변수

*str*  
와이드 문자 문자열입니다.

*Len 함수*  
최대 길이 *str* 현재에 할당 되는 매개 변수 **HString** 개체입니다.

*hstr*  
기존 **HString** 개체입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HString 클래스](../windows/hstring-class.md)