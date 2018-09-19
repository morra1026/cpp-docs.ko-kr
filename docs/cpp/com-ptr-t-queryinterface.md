---
title: _com_ptr_t::QueryInterface | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_ptr_t::QueryInterface
- _com_ptr_t.QueryInterface
dev_langs:
- C++
helpviewer_keywords:
- QueryInterface method [C++]
ms.assetid: d03292f1-6b02-40db-9756-8b0837a97319
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e0add1d8f3fc73f78cee3e10642d7b5a12968a6a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46106875"
---
# <a name="comptrtqueryinterface"></a>_com_ptr_t::QueryInterface

**Microsoft 전용**

호출 된 **QueryInterface** 멤버 함수 `IUnknown` 캡슐화 된 인터페이스 포인터에 대 한 합니다.

## <a name="syntax"></a>구문

```
template<typename _InterfaceType> HRESULT QueryInterface (
   const IID& iid,
   _InterfaceType*& p
) throw ( );
template<typename _InterfaceType> HRESULT QueryInterface (
   const IID& iid,
   _InterfaceType** p
) throw( );
```

#### <a name="parameters"></a>매개 변수

*iid*<br/>
`IID` 인터페이스 포인터입니다.

*p*<br/>
원시 인터페이스 포인터입니다.

## <a name="remarks"></a>설명

호출 `IUnknown::QueryInterface` 지정 된 캡슐화 된 인터페이스 포인터에 대 한 `IID` 결과 원시 인터페이스 포인터를 반환 하 고 *p*합니다. 이 루틴은 성공 또는 실패를 나타내는 HRESULT를 반환 합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_ptr_t 클래스](../cpp/com-ptr-t-class.md)