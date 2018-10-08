---
title: 항목 (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.entry
dev_langs:
- C++
helpviewer_keywords:
- entry attribute
ms.assetid: ba4843e3-d7ad-4b86-9a15-0b4192f0f698
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 95eb37898d4934740e1520df758ed33d3dd4c79a
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48791246"
---
# <a name="entry"></a>entry

DLL의 진입점을 식별 하 여 모듈에는 내보낸된 함수 또는 상수를 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[ entry(id) ]
```

### <a name="parameters"></a>매개 변수

*ID*<br/>
진입점의 ID입니다.

## <a name="remarks"></a>설명

합니다 **항목** c + + 특성에 동일한 기능을 합니다 [항목](/windows/desktop/Midl/entry) MIDL 특성입니다.

## <a name="example"></a>예제

예를 참조 하세요 [idl_module](idl-module.md) 의 사용 예에 대 한 **항목**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|`idl_module` 특성|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)합니다.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)  