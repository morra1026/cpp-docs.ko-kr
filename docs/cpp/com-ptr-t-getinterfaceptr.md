---
title: _com_ptr_t::GetInterfacePtr
ms.date: 11/04/2016
f1_keywords:
- _com_ptr_t::GetInterfacePtr
helpviewer_keywords:
- GetInterfacePtr method [C++]
ms.assetid: 55e3e2c7-c939-48b5-a905-4b9cbefeea7e
ms.openlocfilehash: 6746cc97696968ca59c2771d79573bd71d86df62
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50432478"
---
# <a name="comptrtgetinterfaceptr"></a>_com_ptr_t::GetInterfacePtr

**Microsoft 전용**

캡슐화된 인터페이스 포인터가 반환됩니다.

## <a name="syntax"></a>구문

```
Interface* GetInterfacePtr( ) const throw( ); 
Interface*& GetInterfacePtr() throw();
```

## <a name="remarks"></a>설명

NULL 일 수 있는 캡슐화 된 인터페이스 포인터를 반환 합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_ptr_t 클래스](../cpp/com-ptr-t-class.md)