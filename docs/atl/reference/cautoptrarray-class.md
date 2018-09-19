---
title: CAutoPtrArray 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- CAutoPtrArray
- ATLCOLL/ATL::CAutoPtrArray
- ATLCOLL/ATL::CAutoPtrArray::CAutoPtrArray
dev_langs:
- C++
helpviewer_keywords:
- CAutoPtrArray class
ms.assetid: 880a70da-8c81-4427-8ac6-49aa8d424244
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 23cc8e519fc47173efe413cc687ef48c0dc39945
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46025167"
---
# <a name="cautoptrarray-class"></a>CAutoPtrArray 클래스

이 클래스는 스마트 포인터의 배열을 생성할 때 유용한 메서드를 제공 합니다.

> [!IMPORTANT]
>  이 클래스 및 해당 멤버는 Windows 런타임에서 실행 되는 응용 프로그램에서 사용할 수 없습니다.

## <a name="syntax"></a>구문

```
template <typename E>
class CAutoPtrArray : public CAtlArray<
                        ATL::CAutoPtr<E>,
                        CAutoPtrElementTraits<E>>
```

#### <a name="parameters"></a>매개 변수

*E*<br/>
포인터 형식입니다.

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[CAutoPtrArray::CAutoPtrArray](#cautoptrarray)|생성자입니다.|

## <a name="remarks"></a>설명

이 클래스는 생성자를 제공 하 고 메서드에서 파생 [CAtlArray](../../atl/reference/catlarray-class.md) 하 고 [CAutoPtrElementTraits](../../atl/reference/cautoptrelementtraits-class.md) 스마트 포인터를 저장 하는 컬렉션 클래스 개체의 생성을 지원 합니다.

자세한 내용은 [ATL 컬렉션 클래스](../../atl/atl-collection-classes.md)합니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`CAtlArray`

`CAutoPtrArray`

## <a name="requirements"></a>요구 사항

**헤더:** atlcoll.h

##  <a name="cautoptrarray"></a>  CAutoPtrArray::CAutoPtrArray

생성자입니다.

```
CAutoPtrArray() throw();
```

### <a name="remarks"></a>설명

스마트 포인터 배열을 초기화 합니다.

## <a name="see-also"></a>참고 항목

[CAtlArray 클래스](../../atl/reference/catlarray-class.md)<br/>
[CAutoPtrElementTraits 클래스](../../atl/reference/cautoptrelementtraits-class.md)<br/>
[CAutoPtrList 클래스](../../atl/reference/cautoptrlist-class.md)<br/>
[클래스 개요](../../atl/atl-class-overview.md)
