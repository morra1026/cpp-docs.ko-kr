---
title: include_alias
ms.date: 11/04/2016
f1_keywords:
- vc-pragma.include_alias
- include_alias_CPP
helpviewer_keywords:
- pragmas, include_alias
- include_alias pragma
ms.assetid: 3256d589-12b3-4af0-a586-199e96eabacc
ms.openlocfilehash: 616672d713a9f0ac6eab4be8bce9b178d2510723
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50573171"
---
# <a name="includealias"></a>include_alias

*short_filename* 대신 *long_filename*을 사용할 수 있도록 별칭으로 지정합니다. *long_filename*이 반드시 *short_filename*보다 글자수가 많아야 되는건 아닙니다.

## <a name="syntax"></a>구문

> #<a name="pragma-includealiaslongfilename-shortfilename"></a>pragma include_alias("*long_filename*", "*short_filename*")

> #<a name="pragma-includealiaslongfilename-shortfilename"></a>pragma include_alias(<*long_filename*>, <*short_filename*>)

## <a name="remarks"></a>설명

일반적인 최근 파일시스템은 FAT 파일시스템의 8.3 파일이름 길이 제한보다 더 긴 헤더파일 이름을 가질 수 있습니다. 컴파일러는 두 파일명 중 더 긴 헤더 파일 이름의 처음 8자가 고유하다는 보장이 되지 않기 때문에 더 긴 이름을 8.3으로 자를 수 없습니다. 컴파일러는 `#include`하는 헤더파일 중 *long_filename* 문자열을 만나면 *short_filename*으로 대체하고, *short_filename* 헤더파일을 찾습니다. pragma 선언은 대체하려고 하는 `#include` 지시문 전에 배치되어야 합니다. 다음은 사용예를 보여줍니다.

```cpp
// 두 파일의 처음 8글자는 고유하지 않습니다.
#pragma include_alias( "AppleSystemHeaderQuickdraw.h", "quickdra.h" )
#pragma include_alias( "AppleSystemHeaderFruit.h", "fruit.h" )

#pragma include_alias( "GraphicsMenu.h", "gramenu.h" )

#include "AppleSystemHeaderQuickdraw.h"
#include "AppleSystemHeaderFruit.h"
#include "GraphicsMenu.h"
```

별칭이 올바르게 검색되어 매칭시키기 위해서는 철자, 큰따옴표나 꺾쇠 괄호 까지 지정된 내용과 정확하게 일치해야 합니다. **include_alias** pragma는 파일 이름에 대하여 간단한 문자열 매칭 여부를 수행합니다. 다른 파일 이름의 유효성 검증은 수행되지 않습니다. 다음 예를 살펴보면,

```cpp
#pragma include_alias("mymath.h", "math.h")
#include "./mymath.h"
#include "sys/mymath.h"
```

헤더 파일 문자열이 정확하게 일치하지 않기 때문에 별칭 대체가 수행되지 않습니다. 또한 `/Yu`나 `/Yc` 컴파일러 옵션 또는 `hdrstop` pragma에 대한 인수로 사용되는 헤더파일 이름은 대체되지 않습니다. 예를 들어 소스 파일에 다음 지시문이 포함된 경우,

```cpp
#include <AppleSystemHeaderStop.h>
```

해당 컴파일러 옵션이 부여되어야 합니다.

> /YcAppleSystemHeaderStop.h

**include_alias** pragma를 사용하여 헤더파일 이름을 다른파일 경로로 매핑할 수 있습니다. 예를들면,

```cpp
#pragma include_alias( "api.h", "c:\version1.0\api.h" )
#pragma include_alias( <stdio.h>, <newstdio.h> )
#include "api.h"
#include <stdio.h>
```

큰따옴표로 묶인 파일 이름과 꺾쇠 괄호로 묶인 파일 이름을 섞어 사용하지 마십시오. 예를 들어, `#pragma include_alias` 지시문 두 개가 있다면 컴파일러는 다음 `#include` 지시문에 별칭 파일이름으로 대체하지 않습니다.:

```cpp
#include <api.h>
#include "stdio.h"
```

다음 지시문은 에러가 발생합니다.

```cpp
#pragma include_alias(<header.h>, "header.h")  // 에러
```

에러 메세지에 나오거나 `__FILE__` 매크로가 확장하는 파일이름은 별칭으로 대체가 수행 된 후의 이름입니다. 예를 들어 다음 지시문 뒤 출력을 참조 하세요.

```cpp
#pragma include_alias( "VERYLONGFILENAME.H", "myfile.h" )
#include "VERYLONGFILENAME.H"
```

VERYLONGFILENAME.H에서 다음과 같은 에러가 발생됩니다.

```Output
myfile.h(15) : error C2059 : syntax error
```

전이성은 지원되지 않습니다. 다음과 같은 지시문이 주어진 경우

```cpp
#pragma include_alias( "one.h", "two.h" )
#pragma include_alias( "two.h", "three.h" )
#include "one.h"
```

컴파일러는 three.h가 아니라 two.h 파일을 검색합니다.

## <a name="see-also"></a>참고 항목

[Pragma 지시문 및 __Pragma 키워드](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
