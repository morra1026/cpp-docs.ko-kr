---
title: ODBC 및 데이터베이스 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- database classes [C++], ODBC
- ODBC API functions [C++]
- ODBC classes [C++], MFC database classes
- MFC [C++], ODBC and
ms.assetid: b166f82d-6f85-4556-aac8-fb851235d22c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: bce3140818b46bd6cbb255794a08e9b0fa92fbd4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46114971"
---
# <a name="odbc-and-the-database-classes"></a>ODBC 및 데이터베이스 클래스

일반적으로 해야 사용자가 직접 멤버에서 함수의 ODBC API 함수 호출을 캡슐화 하는 MFC ODBC 데이터베이스 클래스를 [CDatabase](../../mfc/reference/cdatabase-class.md) 하 고 [CRecordset](../../mfc/reference/crecordset-class.md) 클래스입니다. 예를 들어, 복잡 한 ODBC 호출 시퀀스, 저장소 위치, 오류 조건 처리 및 기타 작업에 반환된 된 레코드의 바인딩을 관리 하면 데이터베이스 클래스에서. 결과적으로, 레코드를 레코드 집합 개체를 통해 조작에 상당히 단순 클래스 인터페이스를 사용 합니다.  
  
> [!NOTE]
>  ODBC 데이터 원본 MFC 데이터 액세스 개체 (DAO) 클래스 또는이 항목에 설명 된 대로 MFC ODBC 클래스를 통해 액세스할 수 있습니다.  
  
데이터베이스 클래스 ODBC 기능을 캡슐화 하는 있지만 ODBC API 함수를 한 일대일 매핑을 제공 하지 않습니다. 데이터베이스 클래스를 더 높은 수준의 추상화, Microsoft Access 및 Microsoft Visual Basic에서 데이터 액세스 개체를 찾으면 모델링을 제공 합니다. 자세한 내용은 [ODBC 및 MFC](../../data/odbc/odbc-and-mfc.md)합니다.  
  
## <a name="see-also"></a>참고 항목  

[ODBC 기본 사항](../../data/odbc/odbc-basics.md)