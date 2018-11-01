---
title: _com_error::operator =
ms.date: 11/04/2016
f1_keywords:
- _com_error::operator=
helpviewer_keywords:
- operator= _com_error objects
- = operator [C++], with specific Visual C++ objects
- operator = _com_error objects
ms.assetid: b9cc4094-d055-450c-b45a-0a95317488f8
ms.openlocfilehash: 68eb486ec109d98890ebf3adc0c086368380142b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50449597"
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