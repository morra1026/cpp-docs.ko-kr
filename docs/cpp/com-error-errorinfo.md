---
title: _com_error::ErrorInfo | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_error::ErrorInfo
dev_langs:
- C++
helpviewer_keywords:
- ErrorInfo method [C++]
ms.assetid: 071b446c-4395-4fb8-bd3d-300a8b25f5cd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1fc2906827e6a465106a3dbdcb8b63c7b53a39ee
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039350"
---
# <a name="comerrorerrorinfo"></a>_com_error::ErrorInfo

**Microsoft 전용**

검색 된 `IErrorInfo` 개체 생성자에 전달 합니다.

## <a name="syntax"></a>구문

```
IErrorInfo * ErrorInfo( ) const throw( );
```

## <a name="return-value"></a>반환 값

생성자에 전달된 원시 `IErrorInfo` 항목입니다.

## <a name="remarks"></a>설명

캡슐화 된 검색 `IErrorInfo` 항목에 `_com_error` 개체 또는 없으면 NULL `IErrorInfo` 항목 기록 됩니다. 호출자에 게 호출 해야 `Release` 완료 되 면 반환된 된 개체에이 사용 합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_error 클래스](../cpp/com-error-class.md)