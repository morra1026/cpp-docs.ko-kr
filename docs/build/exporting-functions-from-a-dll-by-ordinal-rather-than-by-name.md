---
title: 이름 대신 서수를 사용하여 DLL에서 함수 내보내기
ms.date: 11/04/2016
f1_keywords:
- NONAME
helpviewer_keywords:
- exporting functions [C++], ordinal values
- ordinal exports [C++]
- exporting DLLs [C++], ordinal values
- NONAME attribute
ms.assetid: 679719fd-d965-4df3-9f7a-7d86ad831702
ms.openlocfilehash: 6a5ac13fdc85b3cb1626aefa28b92866a8c856c1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50503419"
---
# <a name="exporting-functions-from-a-dll-by-ordinal-rather-than-by-name"></a>이름 대신 서수를 사용하여 DLL에서 함수 내보내기

DLL에서 함수를 내보내는 가장 간단한 방법은 이름을 사용하여 함수를 내보내는 것입니다. 예를 들어, **__declspec(dllexport)**을 사용할 때 이 방법이 사용됩니다. 그러나 이름 대신 서수를 사용하여 함수를 내보낼 수도 있습니다. 이 방법을 사용할 경우에는 **__declspec(dllexport)** 대신 .def 파일을 사용해야 합니다. 함수의 서수 값을 지정하려면 .def 파일에서 함수 이름에 서수를 추가합니다. 서수 지정에 대한 자세한 내용은 [.def 파일을 사용하여 DLL에서 내보내기](../build/exporting-from-a-dll-using-def-files.md)를 참조하십시오.

> [!TIP]
>  DLL의 파일 크기를 최적화하려면 내보내는 각 함수에 **NONAME** 특성을 사용합니다. **NONAME** 특성을 사용하면 DLL의 내보내기 테이블에 함수 이름 대신 서수가 저장됩니다. 따라서 많은 함수를 내보내는 경우에 파일 크기를 상당히 줄일 수 있습니다.

## <a name="what-do-you-want-to-do"></a>원하는 작업을 선택하세요.

- [.def 파일을 사용하여 서수로 내보내기](../build/exporting-from-a-dll-using-def-files.md)

- [__declspec(dllexport) 사용](../build/exporting-from-a-dll-using-declspec-dllexport.md)

## <a name="see-also"></a>참고 항목

[DLL에서 내보내기](../build/exporting-from-a-dll.md)
