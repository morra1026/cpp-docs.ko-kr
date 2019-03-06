---
title: IGetDataSourceImpl 클래스
ms.date: 11/04/2016
f1_keywords:
- IGetDataSourceImpl
- ATL.IGetDataSourceImpl<T>
- ATL.IGetDataSourceImpl
- ATL::IGetDataSourceImpl
- ATL::IGetDataSourceImpl<T>
- GetDataSource
- IGetDataSourceImpl.GetDataSource
- IGetDataSourceImpl::GetDataSource
helpviewer_keywords:
- IGetDataSourceImpl class
- GetDataSource method
ms.assetid: d63f3178-d663-4f01-8c09-8aab2dd6805a
ms.openlocfilehash: bb4147bda64e86770e133e10a60efa567cee7719
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57414072"
---
# <a name="igetdatasourceimpl-class"></a>IGetDataSourceImpl 클래스

구현을 제공 합니다 [IGetDataSource](/previous-versions/windows/desktop/ms709721(v=vs.85)) 개체입니다.

## <a name="syntax"></a>구문

```cpp
template <class T>
class ATL_NO_VTABLE IGetDataSourceImpl : public IGetDataSource
```

### <a name="parameters"></a>매개 변수

*T*<br/>
클래스에서 파생 된 `IGetDataSourceImpl`합니다.

## <a name="requirements"></a>요구 사항

**헤더:** atldb.h

## <a name="members"></a>멤버

### <a name="interface-methods"></a>인터페이스 메서드

|||
|-|-|
|[GetDataSource](#getdatasource)|세션을 만든 데이터 원본 개체에 대 한 인터페이스 포인터를 반환 합니다.|

## <a name="remarks"></a>설명

데이터 원본 개체에 대 한 인터페이스 포인터를 가져오는 세션에서 필수 인터페이스입니다.

## <a name="getdatasource"></a> IGetDataSourceImpl::GetDataSource

세션을 만든 데이터 원본 개체에 대 한 인터페이스 포인터를 반환 합니다.

### <a name="syntax"></a>구문

```cpp
STDMETHOD(GetDataSource)(REFIID riid,
   IUnknown ** ppDataSource);
```

#### <a name="parameters"></a>매개 변수

참조 [IGetDataSource::GetDataSource](/previous-versions/windows/desktop/ms725443(v=vs.85)) 에 *OLE DB Programmer's Reference*합니다.

### <a name="remarks"></a>설명

데이터 원본 개체의 속성에 액세스 해야 하는 경우에 유용 합니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)