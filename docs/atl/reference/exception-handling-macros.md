---
title: 예외 처리 매크로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- atldef/ATL::_ATLCATCH
- atldef/ATL::_ATLCATCHALL
- atldef/ATL::_ATLTRY
dev_langs:
- C++
helpviewer_keywords:
- exception handling, macros
- C++ exception handling, macros
ms.assetid: a8385d34-3fb0-4006-a42a-de045cacf0f4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b503e36dfe04eaa3180809033187957ff8d970a0
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43766817"
---
# <a name="exception-handling-macros"></a>예외 처리 매크로

이러한 매크로 예외 처리에 대 한 지원을 제공합니다.

|||
|-|-|
|[_ATLCATCH](#_atlcatch)|연결에서 발생 하는 오류를 처리 하는 문 `_ATLTRY`합니다.|
|[_ATLCATCHALL](#_atlcatchall)|연결에서 발생 하는 오류를 처리 하는 문 `_ATLTRY`합니다.|
|[_ATLTRY](#_atltry)|오류가 발생할 수 있는 수 있는 보호 된 코드 섹션을 표시 합니다.|

## <a name="requirements"></a>요구 사항:

**헤더:** atldef.h

##  <a name="_atlcatch"></a>  _ATLCATCH

연결에서 발생 하는 오류를 처리 하는 문 `_ATLTRY`합니다.

```
_ATLCATCH(e)
```

### <a name="parameters"></a>매개 변수

*e*  
예외 catch입니다.

### <a name="remarks"></a>설명

와 함께 사용할 `_ATLTRY`합니다. C + +로 확인 되 [catch (CAtlException e)](../../cpp/try-throw-and-catch-statements-cpp.md) 특정된 유형의 c + + 예외를 처리 합니다.

##  <a name="_atlcatchall"></a>  _ATLCATCHALL

연결에서 발생 하는 오류를 처리 하는 문 `_ATLTRY`합니다.

```
_ATLCATCHALL
```

### <a name="remarks"></a>설명

와 함께 사용할 `_ATLTRY`합니다. C + + 확인 [catch (...) ](../../cpp/try-throw-and-catch-statements-cpp.md) 모든 유형의 c + + 예외를 처리 합니다.

##  <a name="_atltry"></a>  _ATLTRY

오류가 발생할 수 있는 수 있는 보호 된 코드 섹션을 표시 합니다.

```
_ATLTRY
```

### <a name="remarks"></a>설명

와 함께 사용할 [_ATLCATCH](#_atlcatch) 하거나 [_ATLCATCHALL](#_atlcatchall)합니다. C + + 기호를 확인 [시도](../../cpp/try-throw-and-catch-statements-cpp.md)합니다.

## <a name="see-also"></a>참고 항목

[매크로](../../atl/reference/atl-macros.md)
