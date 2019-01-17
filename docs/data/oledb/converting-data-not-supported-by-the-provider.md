---
title: 공급자가 지원하지 않는 데이터 변환
ms.date: 10/29/2018
helpviewer_keywords:
- OLE DB provider templates, unsupported data types
ms.assetid: f495e50f-530a-4fab-ab54-e0c359785845
ms.openlocfilehash: 44cdde2bad24d21adbc728c90ecd173717c02b04
ms.sourcegitcommit: 943c792fdabf01c98c31465f23949a829eab9aad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2018
ms.locfileid: "51265193"
---
# <a name="converting-data-not-supported-by-the-provider"></a>공급자가 지원하지 않는 데이터 변환

공급자가 지원하지 않는 데이터 형식을 소비자가 요청하면 `IRowsetImpl::GetData`에 대한 OLE DB 공급자 템플릿 코드가 Msdadc.dll을 호출하여 데이터 형식을 변환합니다.

`IRowsetChange`와 같이 데이터 변환이 필요한 인터페이스를 구현할 경우에는 Msdaenum.dll을 호출하여 변환할 수 있습니다. Atldb.h에 정의된 `GetData`를 예제로 사용합니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿을 사용하여 작업](../../data/oledb/working-with-ole-db-provider-templates.md)