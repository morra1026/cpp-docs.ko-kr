---
title: NMAKE 심각한 오류 U1070 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U1070
dev_langs:
- C++
helpviewer_keywords:
- U1070
ms.assetid: 8639fc39-b4b1-48f5-ac91-0e9fb61680fd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b6eb462e5c3c7e497cde55151bf92c62ffb2afcd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46087021"
---
# <a name="nmake-fatal-error-u1070"></a>NMAKE 심각한 오류 U1070

'매크로 이름' 매크로 정의에서 순환 됩니다.

지정 된 매크로 정의는 정의가 지정된 매크로 포함 하는 매크로 포함 되어 있습니다. 순환 매크로 정의 사용할 수 없습니다.

## <a name="example"></a>예제

다음 매크로 정의

```
ONE=$(TWO)
TWO=$(ONE)
```

다음 오류가 발생 합니다.

```
cycle in macro definition 'TWO'
```