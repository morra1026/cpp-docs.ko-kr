---
title: 저장 프로시저 사용
ms.date: 10/24/2018
helpviewer_keywords:
- OLE DB, stored procedures
- stored procedures, Visual C++
- stored procedures, about stored procedures
- OLE DB provider templates, stored procedures
- stored procedures, OLE DB
ms.assetid: 90507e4c-eca2-46c9-ad8c-07e10dc1d41b
ms.openlocfilehash: 2c0c1c71103384439d0b7b94f942e1b5a6d9e651
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50536160"
---
# <a name="using-stored-procedures"></a>저장 프로시저 사용

저장 프로시저는 데이터베이스에 저장된 실행 가능한 개체입니다. 저장 프로시저를 호출하는 것은 SQL 명령을 호출하는 것과 비슷합니다. 클라이언트 응용 프로그램에서 문을 실행하거나 준비하는 대신 데이터 소스에서 저장 프로시저를 사용하면, 성능 향상, 네트워크 오버헤드 감소, 일관성 및 정확성 개선 등의 여러 가지 장점이 있습니다.

저장 프로시저는 원하는 만큼의 입력이나 출력 매개 변수를 가질 수 있으며(매개 변수가 없을 수도 있음) 반환 값을 전달할 수 있습니다. 사용자는 매개 변수 값을 특정 데이터 값으로 하드 코딩하거나 매개 변수 마커(물음표 '?')를 사용할 수도 있습니다.

> [!NOTE]
>  Visual c + +를 사용 하 여 만든 저장된 프로시저를 사용 하 여 컴파일해야 합니다. CLR SQL Server는 `/clr:safe` 컴파일러 옵션입니다.

SQL Server용 OLE DB 공급자(SQLOLEDB)는 데이터를 반환하기 위해 저장 프로시저가 사용하는 다음 메커니즘을 지원합니다.

- 프로시저의 모든 **SELECT** 문은 결과 집합을 생성합니다.

- 프로시저는 출력 매개 변수를 통해 데이터를 반환할 수 있습니다.

- 프로시저에는 정수 반환 코드가 있을 수 있습니다.

> [!NOTE]
> 사용할 수 없습니다 저장된 프로시저 OLE DB provider for Jet 해당 공급자는 저장된 프로시저를 지원 하지 않으므로 쿼리 문자열에는 상수만 사용할 수 있습니다.

## <a name="see-also"></a>참고 항목

[OLE DB 소비자 템플릿 작업](../../data/oledb/working-with-ole-db-consumer-templates.md)