---
title: embedded_idl | Microsoft Docs
ms.custom: ''
ms.date: 10/18/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- embedded_idl
dev_langs:
- C++
helpviewer_keywords:
- embedded_idl attribute
ms.assetid: f1c1c2e8-3872-4172-8795-8d1288a20452
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d7337595111b01ceeec53cc97f11ec2f35a081c5
ms.sourcegitcommit: 0164af5615389ffb1452ccc432eb55f6dc931047
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49808344"
---
# <a name="embeddedidl"></a>embedded_idl

**C + + 전용**

특성에서 생성된 코드를 유지한 상태에서 형식 라이브러리가 .tlh 파일에 작성되도록 지정합니다.

## <a name="syntax"></a>구문

```
embedded_idl[("param")]
```

### <a name="parameters"></a>매개 변수

*param*<br/>
다음 두 값 중 하나일 수 있습니다.

- **emitidl**: typelib에서 가져온 형식 정보가 특성 사용된 프로젝트에 대해 생성 된 IDL에 표시 됩니다.  `embedded_idl`에 대한 매개 변수를 지정하지 않는 경우 이 값이 기본값으로 적용됩니다.

- **no_emitidl**: typelib에서 가져온 형식 정보가 특성 사용된 프로젝트에 대해 생성 된 IDL에 표시 되지 것입니다.

## <a name="example"></a>예제

```cpp
// import_embedded_idl.cpp
// compile with: /LD
#include <windows.h>
[module(name="MyLib2")];
#import "\school\bin\importlib.tlb" embedded_idl("no_emitidl")
```

## <a name="remarks"></a>설명

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)