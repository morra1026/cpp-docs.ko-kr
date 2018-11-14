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
ms.openlocfilehash: 3f20550558a4af4b286aa0de170763df979ffc5d
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556584"
---
# <a name="rowset-object-interfaces"></a>행 집합 개체 인터페이스

다음 표에서 행 집합 개체에 대 한 OLE DB에서 정의 된 필수 및 선택적 인터페이스를 보여 줍니다.

|인터페이스|필수 여부|OLE DB 템플릿에서 구현 되었습니까?|
|---------------|---------------|--------------------------------------|
|[IAccessor](https://docs.microsoft.com/previous-versions/windows/desktop/ms719672(v=vs.85))|필수|예|
|[IColumnsInfo](https://docs.microsoft.com/previous-versions/windows/desktop/ms724541(v=vs.85))|필수|예|
|[IConvertType](https://docs.microsoft.com/previous-versions/windows/desktop/ms715926(v=vs.85))|필수|예|
|[IRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms720986(v=vs.85))|필수|예|
|[IRowsetInfo](https://docs.microsoft.com/previous-versions/windows/desktop/ms724541(v=vs.85))|필수|예|
|[IChapteredRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms718180(v=vs.85))|Optional|아니요|
|[IColumnsInfo2](https://docs.microsoft.com/previous-versions/windows/desktop/ms712953(v=vs.85))|Optional|아니요|
|[IColumnsRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms722657(v=vs.85))|Optional|아니요|
|[IConnectionPointContainer](/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer)|Optional|예 (ATL)|
|[IDBAsynchStatus](https://docs.microsoft.com/previous-versions/windows/desktop/ms709832(v=vs.85))|Optional|아니요|
|[IGetRow](https://docs.microsoft.com/previous-versions/windows/desktop/ms718047(v=vs.85))|Optional|아니요|
|[IRowsetChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms715790(v=vs.85))|Optional|예|
|[IRowsetChapterMember](https://docs.microsoft.com/previous-versions/windows/desktop/ms725430(v=vs.85))|Optional|아니요|
|[IRowsetCurrentIndex](https://docs.microsoft.com/previous-versions/windows/desktop/ms709700(v=vs.85))|Optional|아니요|
|[IRowsetFind](https://docs.microsoft.com/previous-versions/windows/desktop/ms724221(v=vs.85))|Optional|아니요|
|[IRowsetIdentity](https://docs.microsoft.com/previous-versions/windows/desktop/ms715913(v=vs.85))|선택적 (수준 0 공급자에 대 한 필수)|예|
|[IRowsetIndex](https://docs.microsoft.com/previous-versions/windows/desktop/ms719604(v=vs.85))|Optional|아니요|
|[IRowsetLocate](https://docs.microsoft.com/previous-versions/windows/desktop/ms721190(v=vs.85))|Optional|예|
|[IRowsetRefresh](https://docs.microsoft.com/previous-versions/windows/desktop/ms714892(v=vs.85))|Optional|아니요|
|[IRowsetScroll](https://docs.microsoft.com/previous-versions/windows/desktop/ms712984(v=vs.85))|Optional|아니요|
|[IRowsetUpdate](https://docs.microsoft.com/previous-versions/windows/desktop/ms714401(v=vs.85))|Optional|예|
|[IRowsetView](https://docs.microsoft.com/previous-versions/windows/desktop/ms709755(v=vs.85))|Optional|아니요|
|[ISupportErrorInfo](https://docs.microsoft.com/previous-versions/windows/desktop/ms715816(v=vs.85))|Optional|예|
|[IRowsetBookmark](https://docs.microsoft.com/previous-versions/windows/desktop/ms714246(v=vs.85))|Optional|아니요|

마법사에서 생성 된 행 집합 개체에 구현 `IAccessor`, `IRowset`, 및 `IRowsetInfo` 상속을 통해. `IAccessorImpl` 모두 출력 열을 바인딩합니다. `IRowset` 인출 행 및 데이터를 처리 하는 인터페이스입니다. `IRowsetInfo` 행 집합 속성을 처리 하는 인터페이스입니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
