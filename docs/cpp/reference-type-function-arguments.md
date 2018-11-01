---
title: 참조 형식 함수 인수
ms.date: 08/27/2018
helpviewer_keywords:
- arguments [C++], function
- functions [C++], paramters
- function parameters [C++], reference-type
- function arguments [C++], reference-type
- passing parameters [C++], reference-type arguments
ms.assetid: 0a70e831-9e76-46c0-821d-aeba13d73cc0
ms.openlocfilehash: cc5a65e9a6bd74e79856057cf7e7fea220c62d4b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50536206"
---
# <a name="reference-type-function-arguments"></a>참조 형식 함수 인수

보통은 큰 개체보다 참조를 함수에 전달하는 것이 더 효율적입니다. 이렇게 하면 개체에 액세스하는 데 사용된 구문을 유지하면서 컴파일러가 개체의 주소를 전달할 수 있습니다. `Date` 구조체를 사용하는 다음 예제를 살펴보십시오.

```cpp
// reference_type_function_arguments.cpp
#include <iostream>

struct Date
{
    short Month;
    short Day;
    short Year;
};

// Create a date of the form DDDYYYY (day of year, year)
// from a Date.
long DateOfYear( Date& date )
{
    static int cDaysInMonth[] = {
        31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31
    };
    long dateOfYear = 0;

    // Add in days for months already elapsed.
    for ( int i = 0; i < date.Month - 1; ++i )
        dateOfYear += cDaysInMonth[i];

    // Add in days for this month.
    dateOfYear += date.Day;

    // Check for leap year.
    if ( date.Month > 2 &&
        (( date.Year % 100 != 0 || date.Year % 400 == 0 ) &&
        date.Year % 4 == 0 ))
        dateOfYear++;

    // Add in year.
    dateOfYear *= 10000;
    dateOfYear += date.Year;

    return dateOfYear;
}

int main()
{
    Date date{ 8, 27, 2018 };
    long dateOfYear = DateOfYear(date);
    std::cout << dateOfYear << std::endl;
}
```

위의 코드는 참조로 전달 된 구조체의 멤버는 멤버 선택 연산자를 사용 하 여 액세스를 보여 줍니다 (**합니다.**) 대신 포인터 멤버 선택 연산자 (**->**).

포인터 형식의 중요 한 특징 중 하나를 유지 하 고 참조 형식으로 전달 된 인수는 포인터가 아닌 형식의 구문을 준수, 있지만: 이들은로 선언 되지 않은 수정 가능한 **const**합니다. 이 코드에는 `date` 개체를 수정할 의도가 없기 때문에 더 적절한 함수 프로토타입은 다음과 같습니다.

```cpp
long DateOfYear( const Date& date );
```

이 프로토타입은 `DateOfYear` 함수가 인수를 변경하지 않도록 합니다.

표준 변환이 있기 때문에 모든 함수는 참조 형식으로 프로토타입 해당 위치에서 동일한 형식의 개체를 받을 수 있습니다 *typename* 하 *typename* <strong>&</strong>.

## <a name="see-also"></a>참고자료

[참조](../cpp/references-cpp.md)<br/>
