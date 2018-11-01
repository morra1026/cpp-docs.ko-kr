---
title: ODBC 및 SQL 액세스
ms.date: 11/04/2016
helpviewer_keywords:
- API calls [C++], calling DAO or ODBC directly
- Windows API [C++], calling from MFC
- ODBC API functions [C++]
- ODBC API functions [C++], calling from MFC
- SQL [C++], calling ODBC API functions
- ODBC [C++], API functions
ms.assetid: 5613d7dc-00b7-4646-99ae-1116c05c52b4
ms.openlocfilehash: 97aa0f6318a47a93b0079a81dea772b900b5484b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50441771"
---
# <a name="access-to-odbc-and-sql"></a>ODBC 및 SQL 액세스

Microsoft Foundation Class 라이브러리를 대부분 Windows API 호출을 캡슐화 하 고 여전히 모든 Windows API 함수를 직접 호출할 수 있습니다. 데이터베이스 클래스는 ODBC API와 관련 하 여 동일한 유연성을 제공 합니다. 어디에서 나 직접 ODBC API 함수를 호출할 수 있지만 데이터베이스 클래스에는 ODBC의 복잡성에서 보호, 프로그램에서 합니다.

데이터베이스 클래스를 사용 하 여 작업 하는 것과 있습니다으로 보호 되는 마찬가지로 [SQL](../../data/odbc/sql.md), 하지만 원하는 경우 SQL을 직접 사용할 수 있습니다. 사용자 지정 SQL 문 (또는 기본 문의 설정 부분)를 전달 하 여 레코드 집합 개체를 사용자 지정할 수 있습니다 레코드 집합을 열 때. 사용 하 여 직접 SQL 호출도 가능 합니다 [ExecuteSQL](../../mfc/reference/cdatabase-class.md#executesql) 클래스의 멤버 함수 [CDatabase](../../mfc/reference/cdatabase-class.md)합니다.

자세한 내용은 [ODBC: 호출 ODBC API 함수 직접](../../data/odbc/odbc-calling-odbc-api-functions-directly.md) 하 고 [SQL: 만드는 직접 SQL 호출 (ODBC)](../../data/odbc/sql-making-direct-sql-calls-odbc.md)합니다.

## <a name="see-also"></a>참고 항목

[ODBC 및 MFC](../../data/odbc/odbc-and-mfc.md)