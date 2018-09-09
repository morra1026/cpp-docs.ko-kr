---
title: 컴파일러 경고 (수준 1) C4627 | Microsoft Docs
ms.custom: ''
ms.date: 09/09/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4627
dev_langs:
- C++
helpviewer_keywords:
- C4627
ms.assetid: 8840f3e6-b496-423a-8635-eb55d5f854a2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8f6be9ba8ba45adecfe5355848126dcb4b3b2fd1
ms.sourcegitcommit: 592a2f402fef502450a45571a846175cc3ab1ceb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44249622"
---
# <a name="compiler-warning-level-1-c4627"></a>컴파일러 경고(수준 1) C4627

> '*header_file*': 미리 컴파일된 헤더 사용을 찾을 때 건너뛰었습니다

현재 소스 파일에는 [/Yu \(미리 컴파일된 헤더 파일을 사용 하 여)](../../build/reference/yu-use-precompiled-header-file.md) 미리 컴파일된 헤더를 포함 하기 전에 컴파일러가 무시 파일의 모든 항목 집합 옵션입니다. 경고 **C4627** 하는 경우 Visual Studio 2015 및 이전 버전에서 생성 됩니다 *header_file* 미리 컴파일된 헤더 파일, 전에 포함 된 미리 컴파일된 헤더 도포함되지않은경우및*header_file*합니다.

## <a name="example"></a>예제

이 예제는 방법을 보여 주는 오류가 발생할 수 있습니다를 해결 하는 방법을 보여 줍니다.
 
```cpp
// c4627.cpp
#include <iostream>       // C4627 - iostream not included by pch.h
#include "pch.h"          // precompiled header file that does not include iostream
// #include <iostream>    // To fix, move the iostream header include here from above
int main()
{
    std::cout << "std::cout is defined!\n";
}
```
  
## <a name="see-also"></a>참고 항목

[미리 컴파일된 헤더 파일 만들기](../../build/reference/creating-precompiled-header-files.md)
