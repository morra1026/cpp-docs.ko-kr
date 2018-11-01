---
title: 행 집합 개체 인터페이스
ms.date: 10/24/2018
helpviewer_keywords:
- interfaces, OLE DB
- OLE DB, interfaces
- rowset objects [OLE DB]
- OLE DB provider templates, object interfaces
- interfaces, list of
ms.assetid: 0d7a5d48-2fe4-434f-a84b-157c1fdc3494
ms.openlocfilehash: 739c7d94e5df2d5edddc00bd3ae2703e07435c23
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50641014"
---
# <a name="rowset-object-interfaces"></a>행 집합 개체 인터페이스

다음 표에서 행 집합 개체에 대 한 OLE DB에서 정의 된 필수 및 선택적 인터페이스를 보여 줍니다.

|인터페이스|필수 여부|OLE DB 템플릿에서 구현 되었습니까?|
|---------------|---------------|--------------------------------------|
|[IAccessor](/previous-versions/windows/desktop/ms719672)|필수|예|
|[IColumnsInfo](/previous-versions/windows/desktop/ms724541)|필수|예|
|[IConvertType](/previous-versions/windows/desktop/ms715926)|필수|예|
|[IRowset](/previous-versions/windows/desktop/ms720986)|필수|예|
|[IRowsetInfo](/previous-versions/windows/desktop/ms724541)|필수|예|
|[IChapteredRowset](/previous-versions/windows/desktop/ms718180)|Optional|아니요|
|[IColumnsInfo2](/previous-versions/windows/desktop/ms712953)|Optional|아니요|
|[IColumnsRowset](/previous-versions/windows/desktop/ms722657)|Optional|아니요|
|[IConnectionPointContainer](/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer)|Optional|예 (ATL)|
|[IDBAsynchStatus](/previous-versions/windows/desktop/ms709832)|Optional|아니요|
|[IGetRow](/previous-versions/windows/desktop/ms718047)|Optional|아니요|
|[IRowsetChange](/previous-versions/windows/desktop/ms715790)|Optional|예|
|[IRowsetChapterMember](/previous-versions/windows/desktop/ms725430)|Optional|아니요|
|[IRowsetCurrentIndex](/previous-versions/windows/desktop/ms709700)|Optional|아니요|
|[IRowsetFind](/previous-versions/windows/desktop/ms724221)|Optional|아니요|
|[IRowsetIdentity](/previous-versions/windows/desktop/ms715913)|선택적 (수준 0 공급자에 대 한 필수)|예|
|[IRowsetIndex](/previous-versions/windows/desktop/ms719604)|Optional|아니요|
|[IRowsetLocate](/previous-versions/windows/desktop/ms721190)|Optional|예|
|[IRowsetRefresh](/previous-versions/windows/desktop/ms714892)|Optional|아니요|
|[IRowsetScroll](/previous-versions/windows/desktop/ms712984)|Optional|아니요|
|[IRowsetUpdate](/previous-versions/windows/desktop/ms714401)|Optional|예|
|[IRowsetView](/previous-versions/windows/desktop/ms709755)|Optional|아니요|
|[ISupportErrorInfo](/previous-versions/windows/desktop/ms715816)|Optional|예|
|[IRowsetBookmark](/previous-versions/windows/desktop/ms714246)|Optional|아니요|

마법사에서 생성 된 행 집합 개체에 구현 `IAccessor`, `IRowset`, 및 `IRowsetInfo` 상속을 통해. `IAccessorImpl` 모두 출력 열을 바인딩합니다. `IRowset` 인출 행 및 데이터를 처리 하는 인터페이스입니다. `IRowsetInfo` 행 집합 속성을 처리 하는 인터페이스입니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
