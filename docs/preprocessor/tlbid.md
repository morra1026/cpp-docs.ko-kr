---
title: tlbid
ms.date: 10/18/2018
f1_keywords:
- tlbid
helpviewer_keywords:
- tlbid attribute
ms.assetid: 54b06785-191b-4e77-a9a5-485f2b4acb09
ms.openlocfilehash: 31b71f7c195a7e2ee649b40197551e4ff5efda2c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50584514"
---
# <a name="tlbid"></a>tlbid

**C + + 전용**

기본 형식 라이브러리 이외의 라이브러리를 로드할 수 있도록 합니다.

## <a name="syntax"></a>구문

```
tlbid(number)
```

### <a name="parameters"></a>매개 변수

*수*<br/>
`filename`에 있는 형식 라이브러리의 수입니다.

## <a name="remarks"></a>설명

여러 형식 라이브러리를 사용 하 여 기본 형식 라이브러리 이외의 라이브러리를 로드할 수는 단일 DLL에 기본 제공 되는 경우 **tlbid**합니다.

예를 들어:

```cpp
#import <MyResource.dll> tlbid(2)
```

다음과 동일합니다.

```cpp
LoadTypeLib("MyResource.dll\\2");
```

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)