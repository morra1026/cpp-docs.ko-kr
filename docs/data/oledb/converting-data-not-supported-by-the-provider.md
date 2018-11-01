---
title: 공급자가 지원하지 않는 데이터 변환
ms.date: 11/04/2016
helpviewer_keywords:
- OLE DB provider templates, unsupported data types
ms.assetid: f495e50f-530a-4fab-ab54-e0c359785845
ms.openlocfilehash: a53781f71a55dfb07dc996e5e25644d9337e4c63
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50473442"
---
# <a name="converting-data-not-supported-by-the-provider"></a>공급자가 지원하지 않는 데이터 변환

OLE DB 공급자 템플릿에 코드에 대 한 소비자를 요청 하면 공급자가 지원 되지 않는 데이터 형식, `IRowsetImpl::GetData` Msdadc.dll 데이터 형식을 변환을 호출 합니다.

같은 인터페이스를 구현 하는 경우 `IRowsetChange` 데이터 변환을 수행 해야 하는, 변환을 수행 하는 Msdaenum.dll를 호출할 수 있습니다. 사용 하 여 `GetData`예로 Atldb.h에 정의 된 합니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿을 사용하여 작업](../../data/oledb/working-with-ole-db-provider-templates.md)