---
title: IGetDataSourceImpl 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- IGetDataSourceImpl
- ATL.IGetDataSourceImpl<T>
- ATL.IGetDataSourceImpl
- ATL::IGetDataSourceImpl
- ATL::IGetDataSourceImpl<T>
- GetDataSource
- IGetDataSourceImpl.GetDataSource
- IGetDataSourceImpl::GetDataSource
dev_langs:
- C++
helpviewer_keywords:
- IGetDataSourceImpl class
- GetDataSource method
ms.assetid: d63f3178-d663-4f01-8c09-8aab2dd6805a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 9ecc830937e36e213177205549ee4dd4e989e0ed
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118702"
---
# <a name="igetdatasourceimpl-class"></a>IGetDataSourceImpl 클래스

구현을 제공 합니다 [IGetDataSource](/previous-versions/windows/desktop/ms709721\(v=vs.85\)) 개체입니다.  
  
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

## <a name="getdatasource"></a> Igetdatasourceimpl:: Getdatasource

세션을 만든 데이터 원본 개체에 대 한 인터페이스 포인터를 반환 합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp
STDMETHOD(GetDataSource)(REFIID riid,   
   IUnknown ** ppDataSource);  
```  
  
#### <a name="parameters"></a>매개 변수  

참조 [IGetDataSource::GetDataSource](/previous-versions/windows/desktop/ms725443\(v=vs.85\)) 에 *OLE DB Programmer's Reference*합니다.  
  
### <a name="remarks"></a>설명  

데이터 원본 개체의 속성에 액세스 해야 하는 경우에 유용 합니다.  
  
## <a name="see-also"></a>참고 항목  

[OLE DB 공급자 템플릿](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)