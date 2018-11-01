---
title: NMAKE 심각한 오류 U1070
ms.date: 11/04/2016
f1_keywords:
- U1070
helpviewer_keywords:
- U1070
ms.assetid: 8639fc39-b4b1-48f5-ac91-0e9fb61680fd
ms.openlocfilehash: 35bea47f6626dfe283a537d3d96340921c37f3f6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50484216"
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