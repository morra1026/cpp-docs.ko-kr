---
title: 예외 처리기에 대한 제한
ms.date: 11/04/2016
helpviewer_keywords:
- restrictions, exception handlers
- exception handling [C++], exception handlers
ms.assetid: 31d63524-0e8c-419f-b87c-061f4c0ea470
ms.openlocfilehash: 7d5bf20da61f4b9f5012b7f2aab932dfc904c302
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50573994"
---
# <a name="restrictions-on-exception-handlers"></a>예외 처리기에 대한 제한

예외 처리기를 사용 하 여 코드에서의 주요 제한 사항은 사용할 수 없습니다는 **goto** 으로 이동 하는 문을 **__try** 문 블록입니다. 대신, 정상적인 제어 흐름을 통해 문 블록에 들어가야 합니다. 외부로 이동할 수는 **__try** 문을 차단 하 고 선택 하 여 예외 처리기를 중첩 합니다.

## <a name="see-also"></a>참고자료

[예외 처리기 작성](../cpp/writing-an-exception-handler.md)<br/>
[구조적 예외 처리(C/C++)](../cpp/structured-exception-handling-c-cpp.md)