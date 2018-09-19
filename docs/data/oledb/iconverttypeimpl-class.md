---
title: IConvertTypeImpl 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- ATL.IConvertTypeImpl<T>
- IConvertTypeImpl
- ATL.IConvertTypeImpl
- ATL::IConvertTypeImpl
- ATL::IConvertTypeImpl<T>
- IConvertTypeImpl.CanConvert
- CanConvert
- IConvertTypeImpl::CanConvert
dev_langs:
- C++
helpviewer_keywords:
- IConvertTypeImpl class
- CanConvert method
ms.assetid: 7f81e79e-7d3f-4cbe-b93c-d632a94b15f6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: ed4eefe8c05e2b5b027ba1d7c1fec022c9e44409
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46104948"
---
# <a name="iconverttypeimpl-class"></a>IConvertTypeImpl 클래스

구현을 제공 합니다 [IConvertType](/previous-versions/windows/desktop/ms715926\(v=vs.85\)) 인터페이스입니다.  
  
## <a name="syntax"></a>구문

```cpp
template <class T>  
class ATL_NO_VTABLE IConvertTypeImpl   
   : public IConvertType, public CConvertHelper  
```  
  
### <a name="parameters"></a>매개 변수  

*T*<br/>
클래스에서 파생 된 `IConvertTypeImpl`합니다.  

## <a name="requirements"></a>요구 사항  

**헤더:** atldb.h  
  
## <a name="members"></a>멤버  
  
### <a name="interface-methods"></a>인터페이스 메서드  
  
|||  
|-|-|  
|[CanConvert](#canconvert)|명령 또는 행 집합에서 형식 변환의 가용성에 대 한 정보를 제공합니다.|  
  
## <a name="remarks"></a>설명  

이 인터페이스는 명령, 행 집합 및 인덱스 행 집합에 필수입니다. `IConvertTypeImpl` OLE DB에서 제공 된 변환 개체에 위임 하 여 인터페이스를 구현 합니다.  

## <a name="canconvert"></a> Iconverttypeimpl:: Canconvert

명령 또는 행 집합에서 형식 변환의 가용성에 대 한 정보를 제공합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp
STDMETHOD(CanConvert)(DBTYPE wFromType,   
   DBTYPE wToType,   
   DBCONVERTFLAGS dwConvertFlags);  
```  
  
#### <a name="parameters"></a>매개 변수  

참조 [IConvertType::CanConvert](/previous-versions/windows/desktop/ms711224\(v=vs.85\)) 에 *OLE DB Programmer's Reference*합니다.  
  
### <a name="remarks"></a>설명  

OLE DB 데이터 변환을 사용 하 여 `MSADC.DLL`입니다.  
  
## <a name="see-also"></a>참고 항목  

[OLE DB 공급자 템플릿](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)