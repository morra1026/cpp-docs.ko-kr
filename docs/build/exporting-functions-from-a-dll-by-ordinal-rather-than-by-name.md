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

DLL에서 함수 내보내기에 대 한 가장 간단한 방법은 이름으로 내보낼 경우 이 사용 하는 경우 어떻게 되나요 **__declspec (dllexport)** 예를 들어 있습니다. 하지만 대신 서 수로 함수를 내보낼 수 있습니다. 이 기법을 대신.def 파일을 사용 해야 합니다 **__declspec (dllexport)** 합니다. 함수는 서 수 값을 지정 하려면.def 파일의 함수 이름에 해당 서 수를 추가 합니다. 서 수를 지정 하는 방법에 대 한 내용은 [.def 파일을 사용 하 여 DLL에서 내보내기](../build/exporting-from-a-dll-using-def-files.md)합니다.

> [!TIP]
>  DLL의 파일 크기 최적화 하려는 경우 사용 합니다 **NONAME** 내보내는 각 함수에는 특성입니다. 사용 하 여 합니다 **NONAME** 특성의 서 수에 저장 된 DLL의 내보내기 함수는 이름 대신 테이블입니다. 여러 함수를 내보내는 경우 크기를 상당히 줄일 수 있습니다.

## <a name="what-do-you-want-to-do"></a>원하는 작업을 선택하세요.

- [서 수로 내보낼 수 있도록.def 파일을 사용 합니다.](../build/exporting-from-a-dll-using-def-files.md)

- [__Declspec (dllexport)를 사용 합니다.](../build/exporting-from-a-dll-using-declspec-dllexport.md)

## <a name="see-also"></a>참고 항목

[DLL에서 내보내기](../build/exporting-from-a-dll.md)