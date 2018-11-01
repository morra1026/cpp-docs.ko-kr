---
title: 인라인 함수 가져오기 및 내보내기
ms.date: 11/04/2016
helpviewer_keywords:
- exporting functions [C++], inline functions
- inline functions [C++], importing
- DLLs [C++], importing
- importing functions [C++]
- DLLs [C++], exporting from
- importing inline functions [C++]
- inline functions [C++], exporting
- functions [C++], importing
- functions [C++], exporting
ms.assetid: 89f488f8-b078-40fe-afd7-80bd7840057b
ms.openlocfilehash: 407ca39aa53cf622b531fa0ca7818682c82c561f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50439106"
---
# <a name="importing-and-exporting-inline-functions"></a>인라인 함수 가져오기 및 내보내기

가져온된 함수를 인라인으로 정의할 수 있습니다. 효과 대략 표준 함수를 인라인으로; 정의와 같은 함수에 대 한 호출을 매크로 마찬가지로 인라인 코드에 확장 됩니다. C + +를 지 원하는 효율성을 위해 해당 멤버의 일부 함수 인라인 할 수 있는 DLL의 클래스에 주로 유용 합니다.

가져온된 인라인 함수의 기능 중 하나는 c + +에 해당 주소를 가져올 수 있는 경우 컴파일러는 DLL에 상주 하는 인라인 함수의 복사의 주소를 반환 합니다. 또 다른 가져온된 인라인 함수 기능은 전역 가져온된 데이터와 달리, 가져온 함수의 정적 로컬 데이터를 초기화할 수 있습니다.

> [!CAUTION]
>  버전 충돌 가능성이 만들 수 있기 때문에 가져온 인라인 함수를 제공 하는 경우 주의 해야 합니다. 응용 프로그램 코드에 인라인 함수 확장을 가져옵니다. 따라서 함수를 나중에 다시 작성할 때이 업데이트 되지 않습니다 않으면 자체 응용 프로그램이 다시 컴파일됩니다. (일반적으로 DLL 함수 업데이트할 수 있습니다 사용 하는 응용 프로그램을 다시 작성 하지 않고.)

## <a name="what-do-you-want-to-do"></a>원하는 작업을 선택하세요.

- [DLL에서 내보내기](../build/exporting-from-a-dll.md)

- [사용 하 여 DLL에서 내보내기. DEF 파일](../build/exporting-from-a-dll-using-def-files.md)

- [__Declspec (dllexport)을 사용 하 여 DLL에서 내보내기](../build/exporting-from-a-dll-using-declspec-dllexport.md)

- [AFX_EXT_CLASS를 사용 하 여 가져오기 및 내보내기](../build/exporting-and-importing-using-afx-ext-class.md)

- [C 언어 실행 파일에서 사용 하기 위해 c + + 함수 내보내기](../build/exporting-cpp-functions-for-use-in-c-language-executables.md)

- [사용할 내보내기 방법 결정](../build/determining-which-exporting-method-to-use.md)

- [__Declspec (dllimport)을 사용 하 여 응용 프로그램으로 가져오기](../build/importing-into-an-application-using-declspec-dllimport.md)

## <a name="see-also"></a>참고 항목

[가져오기 및 내보내기](../build/importing-and-exporting.md)