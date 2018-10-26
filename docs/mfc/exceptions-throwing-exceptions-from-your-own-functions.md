---
title: '예외: 자체 함수에서 예외를 Throw | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- throwing exceptions [MFC], from functions
- functions [MFC], throwing exceptions
- exceptions [MFC], throwing
ms.assetid: 492976e8-8804-4234-8e8f-30dffd0501be
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: a26bd11c2a37e3644333a95ed03d9182f7b32b87
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50066112"
---
# <a name="exceptions-throwing-exceptions-from-your-own-functions"></a>예외: 자체 함수에서 예외 Throw

MFC 또는 다른 라이브러리의 함수에서 throw 된 예외를 catch 하기 위한 용도로 MFC 예외 처리 패러다임을 사용 하는 것이 가능 합니다. 라이브러리 코드에서 throw 된 예외를 catch 하는 것 외에도 예외 조건에서 발생할 수 있는 함수를 작성 하는 경우 사용자 고유의 코드에서 예외 throw 할 수 있습니다.

예외가 throw 되 면 현재 함수의 실행을 중지 되 고이 직접 이동 하는 합니다 **catch** 가장 안쪽의 예외 프레임의 블록입니다. 예외 메커니즘 함수에서 정상 종료 경로 무시합니다. 따라서 정상 종료에서 삭제 되는 메모리 블록을 삭제 해야 합니다.

#### <a name="to-throw-an-exception"></a>예외를 throw 하려면

1. 와 같은 MFC 도우미 함수 중 하나를 사용 `AfxThrowMemoryException`합니다. 이러한 함수는 적절 한 유형의 미리 할당 된 예외를 throw합니다.

   다음 예제에서는 함수 두 메모리 블록을 할당 하려고에 중 하나를 할당 하지 못한 경우 예외를 throw 합니다.

   [!code-cpp[NVC_MFCExceptions#17](../mfc/codesnippet/cpp/exceptions-throwing-exceptions-from-your-own-functions_1.cpp)]

   첫 번째 할당이 실패 하면 단순히 메모리는 예외를 throw 할 수 있습니다. 첫 번째 할당은 성공 하지만 두 번째 실패 하는 경우에 예외를 throw 하기 전에 첫 번째 할당 블록을 해제 해야 합니다. 모두 할당에 성공할 경우 함수를 종료 하는 경우 블록을 해제 하 고 일반적으로 진행할 수 있습니다.

     - 또는

1. 문제 상태를 표시 하는 사용자 정의 예외를 사용 합니다. 전체 클래스도 모든 형식의 항목 예외로 throw 할 수 있습니다.

   다음 예제에서는 wave 장치를 통해 소리를 재생 하 고 오류가 발생 하는 경우 예외를 throw 합니다.

   [!code-cpp[NVC_MFCExceptions#18](../mfc/codesnippet/cpp/exceptions-throwing-exceptions-from-your-own-functions_2.cpp)]

> [!NOTE]
>  MFC의 기본 처리 하는 예외에 대 한 포인터에만 적용 됩니다 `CException` 개체 (및 개체의 `CException`-파생 클래스). 위의 예제는 MFC의 예외 메커니즘을 무시합니다.

## <a name="see-also"></a>참고 항목

[예외 처리](../mfc/exception-handling-in-mfc.md)

