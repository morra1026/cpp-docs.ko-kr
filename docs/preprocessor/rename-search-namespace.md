---
title: rename_search_namespace | Microsoft Docs
ms.custom: ''
ms.date: 10/18/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- rename_search_namespace
dev_langs:
- C++
helpviewer_keywords:
- rename_search_namespace attribute
ms.assetid: 47c9d7fd-59dc-4c62-87a1-9011a0040167
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f0cc95851c4aa7127e690ec013b9d06d57f2730d
ms.sourcegitcommit: 0164af5615389ffb1452ccc432eb55f6dc931047
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49808890"
---
# <a name="renamesearchnamespace"></a>rename_search_namespace

**C + + 전용**

와 동일한 기능을 [rename_namespace](../preprocessor/rename-namespace.md) 하지만 사용 하는 형식 라이브러리에 사용 되는 `#import` 지시문에 [auto_search](../preprocessor/auto-search.md) 특성.

## <a name="syntax"></a>구문

```
rename_search_namespace("NewName")
```

### <a name="parameters"></a>매개 변수

*NewName*<br/>
네임스페이스의 새 이름입니다.

## <a name="remarks"></a>설명

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)