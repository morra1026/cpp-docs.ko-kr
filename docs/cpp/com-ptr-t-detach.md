---
title: _com_ptr_t::Detach | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_ptr_t::Detach
dev_langs:
- C++
helpviewer_keywords:
- Detach method [C++]
ms.assetid: 0652053e-af37-44e9-a278-2522212ebfed
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: a7f2f44df96ca339e5d8e4b251b5f2d259cb606b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46092143"
---
# <a name="comptrtdetach"></a>_com_ptr_t::Detach

**Microsoft 전용**

캡슐화된 인터페이스 포인터를 추출하고 반환합니다.

## <a name="syntax"></a>구문

```
Interface* Detach( ) throw( );
```

## <a name="remarks"></a>설명

추출 및 캡슐화 된 인터페이스 포인터를 반환 하 고 NULL로 캡슐화 된 포인터 저장소를 지웁니다. 이 작업을 통해 인터페이스 포인터의 캡슐화를 제거합니다. 호출 하는 것 `Release` 반환 된 인터페이스 포인터에 대 한 합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_ptr_t 클래스](../cpp/com-ptr-t-class.md)