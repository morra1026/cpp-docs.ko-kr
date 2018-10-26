---
title: (C + +) 생성자 없이 클래스 및 구조체 초기화 | Microsoft Docs
ms.custom: ''
ms.date: 10/17/2018
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
ms.assetid: 3e55c3d6-1c6b-4084-b9e5-221b151402f4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: fb72bf8c8550d87a4e6bf86e440c7a468f4f878d
ms.sourcegitcommit: f9d9db80a8f13eae2c41337b974e1298109e33c5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2018
ms.locfileid: "49640759"
---
# <a name="initializing-classes-and-structs-without-constructors-c"></a>생성자 없이 클래스 및 구조체 초기화(C++)

클래스, 특히 비교적 간단한 클래스에 대해 항상 생성자를 정의할 필요는 없습니다. 사용자는 다음 예제와 같이 균일 초기화를 사용하여 클래스 또는 구조체의 개체를 초기화할 수 있습니다.

```cpp
// no_constructor.cpp
// Compile with: cl /EHsc no_constructor.cpp
#include <time.h>

// No constructor
struct TempData
{
    int StationId;
    time_t timeSet;
    double current;
    double maxTemp;
    double minTemp;
};

// Has a constructor
struct TempData2
{
    TempData2(double minimum, double maximum, double cur, int id, time_t t) :
       stationId{id}, timeSet{t}, current{cur}, maxTemp{maximum}, minTemp{minimum} {}
    int stationId;
    time_t timeSet;
    double current;
    double maxTemp;
    double minTemp;
};

int main()
{
    time_t time_to_set;

    // Member initialization (in order of declaration):
    TempData td{ 45978, time(&time_to_set), 28.9, 37.0, 16.7 };

    // Default initialization = {0,0,0,0,0}
    TempData td_default{};

    // Uninitialized = if used, emits warning C4700 uninitialized local variable
    TempData td_noInit;

    // Member declaration (in order of ctor parameters)
    TempData2 td2{ 16.7, 37.0, 28.9, 45978, time(&time_to_set) };

    return 0;
}
```

클래스 또는 구조체에 생성자가 없는 경우 제공 하는 멤버 클래스에서 선언 되는 순서로 목록 요소를 참고 합니다. 클래스에 생성자가 하는 경우 매개 변수를 순서 대로 요소를 제공 합니다.

## <a name="see-also"></a>참고자료

[클래스 및 구조체](../cpp/classes-and-structs-cpp.md)<br/>
[생성자](../cpp/constructors-cpp.md)
