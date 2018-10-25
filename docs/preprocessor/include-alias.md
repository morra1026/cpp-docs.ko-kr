---
title: include_alias | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- vc-pragma.include_alias
- include_alias_CPP
dev_langs:
- C++
helpviewer_keywords:
- pragmas, include_alias
- include_alias pragma
ms.assetid: 3256d589-12b3-4af0-a586-199e96eabacc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c9844c610a1b5bffab8f5fba67daff90a52412e4
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50065176"
---
# <a name="includealias"></a>include_alias

형식임 *short_filename* 별칭으로 사용할 *long_filename*합니다.

## <a name="syntax"></a>구문

> #<a name="pragma-includealiaslongfilename-shortfilename"></a>pragma include_alias("*long_filename*", "*short_filename*")
> #<a name="pragma-includealiaslongfilename-shortfilename"></a>pragma include_alias(*long_filename*, *short_filename*)

## <a name="remarks"></a>설명

일부 파일 시스템의 경우 8.3 FAT 파일 시스템 제한보다 더 긴 헤더 파일 이름을 가질 수 있습니다. 더 긴 헤더 파일 이름의 첫 8개 문자가 고유하지 않을 수 있기 때문에 컴파일러는 더 긴 이름을 8.3으로 간단히 자를 수 없습니다. 컴파일러가 합니다 *long_filename* 대체 문자열 *short_filename*, 및 헤더 파일을 찾습니다 *short_filename* 대신 합니다. 이 pragma는 해당 `#include` 지시문 앞에 배치되어야 합니다. 예:

```cpp
// First eight characters of these two files not unique.
#pragma include_alias( "AppleSystemHeaderQuickdraw.h", "quickdra.h" )
#pragma include_alias( "AppleSystemHeaderFruit.h", "fruit.h" )

#pragma include_alias( "GraphicsMenu.h", "gramenu.h" )

#include "AppleSystemHeaderQuickdraw.h"
#include "AppleSystemHeaderFruit.h"
#include "GraphicsMenu.h"
```

검색된 별칭은 철자, 큰따옴표 또는 꺾쇠 괄호 사용에서 지정된 내용과 정확하게 일치해야 합니다. 합니다 **include_alias** pragma는 파일 이름에 대해 일치 하는 간단한 문자열; 없는 다른 파일 이름 유효성 검사를 수행 합니다. 예를 들어 다음과 같은 지시문에서는

```cpp
#pragma include_alias("mymath.h", "math.h")
#include "./mymath.h"
#include "sys/mymath.h"
```

헤더 파일 문자열이 정확하게 일치하지 않기 때문에 별칭 대체가 수행되지 않습니다. 또한 헤더 파일에 대 한 인수로 사용 합니다 `/Yu` 및 `/Yc` 컴파일러 옵션 또는 `hdrstop` pragma를 대체 되지 않습니다. 예를 들어 소스 파일에 다음 지시문이 포함된 경우,

```cpp
#include <AppleSystemHeaderStop.h>
```

해당 컴파일러 옵션은 다음과 같이 됩니다.

> /YcAppleSystemHeaderStop.h

사용할 수는 **include_alias** 다른 모든 헤더 파일 이름에 매핑할 pragma입니다. 예를 들어:

```cpp
#pragma include_alias( "api.h", "c:\version1.0\api.h" )
#pragma include_alias( <stdio.h>, <newstdio.h> )
#include "api.h"
#include <stdio.h>
```

큰따옴표로 묶인 파일 이름과 꺾쇠 괄호로 묶인 파일 이름을 섞어 사용하지 마십시오. 예를 들어, 위의 두 가지를 제공 `#pragma include_alias` 다음에 없는 대체를 수행 하는 컴파일러 지시문 `#include` 지시문:

```cpp
#include <api.h>
#include "stdio.h"
```

또한 다음 지시문은 오류를 생성합니다.

```cpp
#pragma include_alias(<header.h>, "header.h")  // Error
```

미리 정의 된 값 또는 오류 메시지에 파일 이름을 보고 `__FILE__` 대체가 수행 된 후 매크로 파일의 이름입니다. 예를 들어 다음 지시문 뒤 출력을 참조 하세요.

```cpp
#pragma include_alias( "VeryLongFileName.H", "myfile.h" )
#include "VeryLongFileName.H"
```

VERYLONGFILENAME에 오류가 있습니다. H 다음 오류 메시지가 생성 됩니다.

```Output
myfile.h(15) : error C2059 : syntax error
```

또한 전이성은 지원되지 않습니다. 다음과 같은 지시문이 주어진 경우

```cpp
#pragma include_alias( "one.h", "two.h" )
#pragma include_alias( "two.h", "three.h" )
#include "one.h"
```

컴파일러는 THREE.H가 아니라 TWO.H 파일을 검색합니다.

## <a name="see-also"></a>참고 항목

[Pragma 지시문 및 __Pragma 키워드](../preprocessor/pragma-directives-and-the-pragma-keyword.md)