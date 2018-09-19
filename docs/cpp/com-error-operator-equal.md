---
title: _com_error::operator = | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_error::operator=
dev_langs:
- C++
helpviewer_keywords:
- operator= _com_error objects
- = operator [C++], with specific Visual C++ objects
- operator = _com_error objects
ms.assetid: b9cc4094-d055-450c-b45a-0a95317488f8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c2fe53c7040bc248d63bd3d14f90f915bdcd689a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46061034"
---
# <a name="comerroroperator-"></a>_com_error::operator =

**Microsoft 전용**

기존 `_com_error` 개체를 다른 개체에 할당합니다.

## <a name="syntax"></a>구문

```
_com_error& operator = (
   const _com_error& that
) throw ( );
```

#### <a name="parameters"></a>매개 변수

*는*<br/>
`_com_error` 개체입니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_error 클래스](../cpp/com-error-class.md)