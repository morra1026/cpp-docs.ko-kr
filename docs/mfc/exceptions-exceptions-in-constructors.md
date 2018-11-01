---
title: '예외: 생성자의 예외'
ms.date: 11/04/2016
helpviewer_keywords:
- constructors [MFC], exceptions
- throwing exceptions [MFC], in constructors
- exceptions [MFC], in constructors
ms.assetid: a78eae5a-5821-4b27-9478-1436320ed1e1
ms.openlocfilehash: 23d1f6a9a3c76cc9c0c1d4aebd5c0b0ea45c3154
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50472272"
---
# <a name="exceptions-exceptions-in-constructors"></a>예외: 생성자의 예외

생성자에서는 예외를 throw 하는 경우에 설명 된 대로 예외를 throw 하기 전에 내용을 모든 개체 및 메모리 할당 정리 [예외: 사용자 고유의 함수에서 예외 Throw](../mfc/exceptions-throwing-exceptions-from-your-own-functions.md)합니다.

생성자에서는 예외를 throw 하는 경우 개체 자체에 대 한 메모리가 이미 생성자가 호출에 의해 할당 되었습니다. 따라서 컴파일러는 자동으로 메모리 할당을 취소는 예외가 throw 된 후 개체가 차지 합니다.

자세한 내용은 [예외: 예외의 개체 해제](../mfc/exceptions-freeing-objects-in-exceptions.md)합니다.

## <a name="see-also"></a>참고 항목

[예외 처리](../mfc/exception-handling-in-mfc.md)

