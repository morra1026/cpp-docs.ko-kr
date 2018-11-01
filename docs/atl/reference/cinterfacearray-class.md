---
title: CInterfaceArray 클래스
ms.date: 11/04/2016
f1_keywords:
- CInterfaceArray
- ATLCOLL/ATL::CInterfaceArray
- ATLCOLL/ATL::CInterfaceArray::CInterfaceArray
helpviewer_keywords:
- CInterfaceArray class
ms.assetid: 1f29cf66-a086-4a7b-b6a8-64f73da39f79
ms.openlocfilehash: 64271cbdb634284a5abcdd17b2c14d23a496b3f5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50614254"
---
# <a name="cinterfacearray-class"></a>CInterfaceArray 클래스

이 클래스는 COM 인터페이스 포인터의 배열을 생성할 때 유용한 메서드를 제공 합니다.

## <a name="syntax"></a>구문

```
template <class I, const IID* piid=& __uuidof(I)>
class CInterfaceArray :
   public CAtlArray<ATL::CComQIPtr<I, piid>,
                    CComQIPtrElementTraits<I, piid>>
```

#### <a name="parameters"></a>매개 변수

*I*<br/>
저장에 대 한 포인터의 형식을 지정 하는 COM 인터페이스입니다.

*piid*<br/>
에 대 한 포인터의 IID *있습니까*합니다.

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[CInterfaceArray::CInterfaceArray](#cinterfacearray)|인터페이스 배열에 대 한 생성자입니다.|

## <a name="remarks"></a>설명

이 클래스는 생성자 및 COM 인터페이스 포인터의 배열을 만드는 방법에 대 한 파생된 메서드를 제공 합니다. 사용 하 여 [CInterfaceList](../../atl/reference/cinterfacelist-class.md) 목록이 필요한 경우.

자세한 내용은 [ATL 컬렉션 클래스](../../atl/atl-collection-classes.md)합니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`CAtlArray`

`CInterfaceArray`

## <a name="requirements"></a>요구 사항

**헤더:** atlcoll.h

##  <a name="cinterfacearray"></a>  CInterfaceArray::CInterfaceArray

생성자입니다.

```
CInterfaceArray() throw();
```

### <a name="remarks"></a>설명

스마트 포인터 배열을 초기화 합니다.

## <a name="see-also"></a>참고 항목

[CAtlArray 클래스](../../atl/reference/catlarray-class.md)<br/>
[CComQIPtr 클래스](../../atl/reference/ccomqiptr-class.md)<br/>
[CComQIPtrElementTraits 클래스](../../atl/reference/ccomqiptrelementtraits-class.md)<br/>
[클래스 개요](../../atl/atl-class-overview.md)
