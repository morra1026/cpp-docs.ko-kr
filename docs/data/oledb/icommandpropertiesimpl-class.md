---
title: ICommandPropertiesImpl 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- ICommandPropertiesImpl
- ATL.ICommandPropertiesImpl
- ATL::ICommandPropertiesImpl
- ICommandPropertiesImpl::GetProperties
- ICommandPropertiesImpl.GetProperties
- GetProperties
- ICommandPropertiesImpl.SetProperties
- ICommandPropertiesImpl::SetProperties
- SetProperties
dev_langs:
- C++
helpviewer_keywords:
- ICommandPropertiesImpl class
- GetProperties method
- SetProperties method
ms.assetid: b3cf6aea-527e-4f0d-96e0-669178b021a2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 40c1648131db04ed1629da453a16112debf6e6be
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50053599"
---
# <a name="icommandpropertiesimpl-class"></a>ICommandPropertiesImpl 클래스

구현을 제공 합니다 [ICommandProperties](/previous-versions/windows/desktop/ms723044) 인터페이스입니다.

## <a name="syntax"></a>구문

```cpp
template <class T, class PropClass = T>
class ATL_NO_VTABLE ICommandPropertiesImpl
   : public ICommandProperties, public CUtlProps<PropClass>
```

### <a name="parameters"></a>매개 변수

*T*<br/>
파생 된 클래스

*PropClass*<br/>
속성 클래스입니다.

## <a name="requirements"></a>요구 사항

**헤더:** atldb.h

## <a name="members"></a>멤버

### <a name="interface-methods"></a>인터페이스 메서드

|||
|-|-|
|[GetProperties](#getproperties)|현재 행 집합에 대 한 요청 된 행 집합 속성 그룹의 속성 목록을 반환 합니다.|
|[SetProperties](#setproperties)|행 집합 속성 그룹의 속성을 설정합니다.|

## <a name="remarks"></a>설명

이 명령에 필수입니다. 구현이 정의 된 정적 함수에서 제공 되는 [BEGIN_PROPSET_MAP](../../data/oledb/begin-propset-map.md) 매크로입니다.

## <a name="getproperties"></a> Icommandpropertiesimpl:: Getproperties

명령의 속성 맵을 사용 하 여 모든 요청 된 속성 집합을 반환 합니다.

### <a name="syntax"></a>구문

```cpp
STDMETHOD(GetProperties)(const ULONG cPropertyIDSets, 
   const DBPROPIDSET rgPropertyIDSets[], 
   ULONG * pcPropertySets, 
   DBPROPSET ** prgPropertySets);
```

#### <a name="parameters"></a>매개 변수

참조 [icommandproperties:: Getproperties](/previous-versions/windows/desktop/ms723119) 에 *OLE DB Programmer's Reference*합니다.

### <a name="remarks"></a>설명

[BEGIN_PROPSET_MAP](../../data/oledb/begin-propset-map.md)을 참조하세요.

## <a name="setproperties"></a> Icommandpropertiesimpl:: Setproperties

명령 개체에 대 한 속성을 설정합니다.

### <a name="syntax"></a>구문

```cpp
STDMETHOD(SetProperties)(ULONG cPropertySets, 
   DBPROPSET rgPropertySets[]);
```

#### <a name="parameters"></a>매개 변수

참조 [icommandproperties:: Setproperties](/previous-versions/windows/desktop/ms711497) 에 *OLE DB Programmer's Reference*합니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)