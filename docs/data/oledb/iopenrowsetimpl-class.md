---
title: IOpenRowsetImpl 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- IOpenRowsetImpl
- IOpenRowsetImpl.CreateRowset
- IOpenRowsetImpl::CreateRowset
- CreateRowset
- OpenRowset
- IOpenRowsetImpl::OpenRowset
- IOpenRowsetImpl.OpenRowset
dev_langs:
- C++
helpviewer_keywords:
- IOpenRowsetImpl class
- CreateRowset method
- OpenRowset method
ms.assetid: d259cedc-1db4-41cf-bc9f-5030907ab486
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 72ca35ad6f2246a517c8a8d103c1a7f37e142534
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50063434"
---
# <a name="iopenrowsetimpl-class"></a>IOpenRowsetImpl 클래스

에 대 한 구현을 제공 합니다 `IOpenRowset` 인터페이스입니다.

## <a name="syntax"></a>구문

```cpp
template <class SessionClass>
class IOpenRowsetImpl : public IOpenRowset
```

### <a name="parameters"></a>매개 변수

*SessionClass*<br/>
클래스에서 파생 된 `IOpenRowsetImpl`합니다.

## <a name="requirements"></a>요구 사항

**헤더:** atldb.h

## <a name="members"></a>멤버

### <a name="methods"></a>메서드

|||
|-|-|
|[CreateRowset](#createrowset)|행 집합 개체를 만듭니다. 사용자가 직접 호출 되지 않습니다.|
|[OpenRowset](#openrowset)|페이지를 열고 단일 기본 테이블 또는 인덱스에서 모든 행이 포함 된 행 집합을 반환 합니다. (ATLDB에 없음. H)|

## <a name="remarks"></a>설명

합니다 [IOpenRowset](/previous-versions/windows/desktop/ms716946) 인터페이스는 세션 개체에 대 한 필수입니다. 열고 단일 기본 테이블 또는 인덱스에서 모든 행이 포함 된 행 집합을 반환 합니다.

## <a name="createrowset"></a> Iopenrowsetimpl:: Createrowset

행 집합 개체를 만듭니다. 사용자가 직접 호출 되지 않습니다. 참조 [iopenrowset:: Openrowset](/previous-versions/windows/desktop/ms716724) 에 *OLE DB 프로그래머 참조입니다.*

### <a name="syntax"></a>구문

```cpp
template template <class RowsetClass>
HRESULT CreateRowset(IUnknown* pUnkOuter,
   DBID* pTableID,
   DBID* pIndexID,
   REFIID riid,
   ULONG cPropertySets,
   DBPROPSET rgPropertySets[],
   IUnknown** ppRowset,
   RowsetClass*& pRowsetObj);
```

#### <a name="parameters"></a>매개 변수

*RowsetClass*<br/>
사용자의 행 집합 클래스를 나타내는 템플릿 클래스 멤버입니다. 일반적으로 마법사에서 생성 됩니다.

*pRowsetObj*<br/>
[out] 행 집합 개체에 대 한 포인터입니다. 일반적으로이 매개 변수는 사용 되지 않지만 COM 개체를 전달 하기 전에 행 집합에서 더 많은 작업을 수행 해야 하는 경우 사용할 수 있습니다. 수명을 *pRowsetObj* 바인딩된 *ppRowset*합니다.

다른 매개 변수를 참조 하세요 [iopenrowset:: Openrowset](/previous-versions/windows/desktop/ms716724) 에 *OLE DB 프로그래머 참조입니다.*

## <a name="openrowset"></a> Iopenrowsetimpl:: Openrowset

페이지를 열고 단일 기본 테이블 또는 인덱스에서 모든 행이 포함 된 행 집합을 반환 합니다.

### <a name="syntax"></a>구문

```cpp
HRESULT OpenRowset(IUnknown* pUnkOuter,
   DBID* pTableID,
   DBID* pIndexID,
   REFIID riid,
   ULONG cPropertySets,
   DBPROPSET rgPropertySets[],
   IUnknown** ppRowset);
```

#### <a name="parameters"></a>매개 변수

참조 [iopenrowset:: Openrowset](/previous-versions/windows/desktop/ms716724) 에 *OLE DB Programmer's Reference*합니다.

### <a name="remarks"></a>설명

이 메서드는 ATLDB에서 찾을 수 없습니다. 8. 공급자를 만들 때 ATL 개체 마법사에서 생성 됩니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)