---
title: 프로그래밍 방식으로 ODBC 데이터 원본에 테이블을 만들려면
ms.date: 11/04/2016
helpviewer_keywords:
- programmatically creating ODBC tables [C++]
- tables [C++]
- ODBC data sources, creating tables in
- tables [C++], creating programmatically
ms.assetid: 9ca68fb5-c3df-424a-a75c-e3fb01cc1b18
ms.openlocfilehash: 139efb7a34baacb2bb6ad424d13f2d337eb12af6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50661658"
---
# <a name="data-source-programmatically-creating-a-table-in-an-odbc-data-source"></a>데이터 소스: ODBC 데이터 소스에서 프로그래밍 방식으로 테이블 작성

이 항목에서는 데이터에 대 한 테이블을 만드는 방법에 설명 소스를 사용 하 여를 `ExecuteSQL` 클래스의 멤버 함수 `CDatabase`, 전달 함수가 포함 된 문자열을 **CREATE TABLE** SQL 문을.

MFC의 ODBC 데이터 원본에 대 한 일반적인 정보를 참조 하세요 [데이터 원본 (ODBC)](../../data/odbc/data-source-odbc.md)합니다. 항목 [데이터 소스: 프로그래밍 방식으로 ODBC 데이터 소스 구성](../../data/odbc/data-source-programmatically-configuring-an-odbc-data-source.md) 만들기 데이터 원본에 설명 합니다.

데이터 원본 설정 된 경우 테이블을 사용 하 여 쉽게 만들 수 있습니다 합니다 `ExecuteSQL` 멤버 함수 및 **CREATE TABLE** SQL 문입니다. 예를 들어 있다면을 `CDatabase` 라는 개체 `myDB`, 테이블을 만들려면 다음과 같은 MFC 코드를 사용할 수 있습니다.

```
myDB.ExecuteSQL("CREATE TABLE OFFICES (OfficeID TEXT(4)" ",
                         OfficeName TEXT(10))");
```

이 코드 예제에서는 Microsoft Access 데이터 원본 연결에서 유지 관리에서 "사무실" 이라는 테이블 `myDB`; 테이블 "OfficeID" 및 "OfficeName." 라는 두 필드를 포함 합니다.

> [!NOTE]
>  에 지정 된 필드 형식 합니다 **CREATE TABLE** SQL 문을 사용 하는 ODBC 드라이버에 따라 달라질 수 있습니다. (Visual c + + 1.5를 사용 하 여 분산) Microsoft 쿼리 프로그램이 데이터 원본에 대해 사용할 수 있는 필드 형식을 검색 하는 한 가지 방법은 합니다. Microsoft 쿼리를 클릭 **파일**, 클릭 **정의**데이터 원본에서 테이블을 선택 하 고에 표시 된 형식을 확인 합니다 **형식** 콤보 상자입니다. SQL 구문 인덱스를 만들 수도 있습니다.

## <a name="see-also"></a>참고 항목

[데이터 소스(ODBC)](../../data/odbc/data-source-odbc.md)