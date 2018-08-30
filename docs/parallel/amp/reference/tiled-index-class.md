---
title: tiled_index 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-amp
ms.topic: reference
f1_keywords:
- tiled_index
- AMP/tiled_index
- AMP/Concurrency::tiled_index::tiled_index
- AMP/Concurrency::tiled_index::get_tile_extent
- AMP/Concurrency::tiled_index::barrier
- AMP/Concurrency::tiled_index::global
- AMP/Concurrency::tiled_index::local
- AMP/Concurrency::tiled_index::rank
- AMP/Concurrency::tiled_index::tile
- AMP/Concurrency::tiled_index::tile_dim0
- AMP/Concurrency::tiled_index::tile_dim1
- AMP/Concurrency::tiled_index::tile_dim2
- AMP/Concurrency::tiled_index::tile_origin
- AMP/Concurrency::tiled_index::tile_extent
dev_langs:
- C++
helpviewer_keywords:
- tiled_index class
ms.assetid: 0ce2ae26-f1bb-4436-b473-a9e1b619bb38
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4ed19dd2a1b62a3682d96f8c9a596fa6a4b1b377
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43209435"
---
# <a name="tiledindex-class"></a>tiled_index 클래스
인덱스를 제공 된 [tiled_extent](tiled-extent-class.md) 개체입니다. 이 클래스는 로컬 타일 원본에 상대적인 및 전역 원본과 요소에 액세스 하는 속성에 있습니다. 바둑판식된 공간에 대 한 자세한 내용은 참조 하세요. [를 사용 하 여 타일](../../../parallel/amp/using-tiles.md)합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <
    int _Dim0,  
    int _Dim1 = 0,  
    int _Dim2 = 0  
>  
class tiled_index : public _Tiled_index_base<3>;  
 
template <
    int _Dim0,  
    int _Dim1  
>  
class tiled_index<_Dim0, _Dim1, 0> : public _Tiled_index_base<2>;  
 
template <
    int _Dim0  
>  
class tiled_index<_Dim0, 0, 0> : public _Tiled_index_base<1>;  
```  
  
#### <a name="parameters"></a>매개 변수  
 `_Dim0`  
 최대 유효 치수의 길이입니다.  
  
 `_Dim1`  
 다음 최대 유효 치수의 길이입니다.  
  
 `_Dim2`  
 최소 유효 치수의 길이입니다.  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[tiled_index 생성자](#ctor)|`tile_index` 클래스의 새 인스턴스를 초기화합니다.|  

  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[get_tile_extent](#tiled_index__get_tile_extent)|반환을 [익스텐트](extent-class.md) 의 값을 가진 개체를 `tiled_index` 템플릿 인수 `_Dim0`, `_Dim1`, 및 `_Dim2`합니다.|  


  
### <a name="public-constants"></a>공용 상수  
  
|이름|설명|  
|----------|-----------------|  
|[barrier 상수](#tiled_index__barrier)|저장소를 [tile_barrier](tile-barrier-class.md) 스레드의 현재 타일에 장애물을 나타내는 개체입니다.|  
|||  
|[전역 상수](#tiled_index__global)|저장소를 [인덱스](index-class.md) 의 인덱스를 전역를 나타내는 차수 1, 2 또는 3의 개체를 [그리드](https://msdn.microsoft.com/f7d1b6a6-586c-4345-b09a-bfc26c492cb0) 개체입니다.|  
|[지역 상수](#tiled_index__local)|저장소를 `index` 의 현재 타일의 상대를 나타내는 차수 1, 2 또는 3 인덱스의 개체를 [tiled_extent](tiled-extent-class.md) 개체입니다.|  
|[rank 상수](#tiled_index__rank)|차수를 저장 합니다 `tiled_index` 개체입니다.|  
|[tile 상수](#tiled_index__tile)|저장소를 `index` 차수 1, 2 또는 3의 현재 타일의 좌표를 나타내는 개체를 `tiled_extent` 개체입니다.|  
|[tile_dim0 Constant](#tiled_index__tile_dim0)|최대 유효 치수의 길이 저장 합니다.|  
|[tile_dim1 상수](#tiled_index__tile_dim1)|다음 최대 유효 치수의 길이 저장 합니다.|  
|[tile_dim2 Constant](#tiled_index__tile_dim2)|최소 유효 치수의 길이 저장 합니다.|  
|[tile_origin 상수](#tiled_index__tile_origin)|저장소를 `index` 개체의 현재 타일의 원점의 전역를 나타내는 차수 1, 2 또는 3 좌표는 `tiled_extent` 개체입니다.|  

  
### <a name="public-data-members"></a>공용 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|[tile_extent](#tile_extent)|가져옵니다는 [익스텐트](extent-class.md) 의 값을 가진 개체를 `tiled_index` 템플릿 인수 `tiled_index` 템플릿 인수 `_Dim0`, `_Dim1`, 및 `_Dim2`합니다.|  

  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `_Tiled_index_base`  
  
 `tiled_index`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** amp.h  
  
 **네임스페이스:** 동시성  


## <a name="tiled_index__ctor"></a>  tiled_index 생성자  
`tiled_index` 클래스의 새 인스턴스를 초기화합니다.  
  
## <a name="syntax"></a>구문  
  
```  
tiled_index(  
    const index<rank>& _Global,  
    const index<rank>& _Local,  
    const index<rank>& _Tile,  
    const index<rank>& _Tile_origin,  
    const tile_barrier& _Barrier ) restrict(amp,cpu);  
  
tiled_index(  
    const tiled_index& _Other ) restrict(amp,cpu);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `_Global`  
 전역 [인덱스](index-class.md) 생성 된 `tiled_index`합니다.  
  
 `_Local`  
 로컬 [인덱스](index-class.md) 생성 된 `tiled_index`  
  
 `_Tile`  
 타일 [인덱스](index-class.md) 생성 된 `tiled_index`  
  
 `_Tile_origin`  
 타일 원본 [인덱스](index-class.md) 생성 된 `tiled_index`  
  
 `_Barrier`  
 합니다 [tile_barrier](tile-barrier-class.md) 생성 된 개체 `tiled_index`합니다.  
  
 `_Other`  
 합니다 `tile_index` 복사할 개체를 생성 된 `tiled_index`합니다.  
  
## <a name="overloads"></a>Overloads  
  
|||  
|-|-|  
|name|설명|  
|`tiled_index(const index<rank>& _Global, const index<rank>& _Local, const index<rank>& _Tile, const index<rank>& _Tile_origin, const tile_barrier& _Barrier restrict(amp,cpu);`|새 인스턴스를 초기화 합니다 `tile_index` 전역 좌표의 타일 및 로컬 좌표의 타일의 상대 위치를 인덱스에서 클래스입니다. 합니다 `_Global` 고 `_Tile_origin` 매개 변수에서 계산 됩니다.|  
|`tiled_index(    const tiled_index& _Other) restrict(amp,cpu);`|새 인스턴스를 초기화 합니다 `tile_index` 지정 된 복사 하 여 클래스 `tiled_index` 개체입니다.|  


## <a name="tiled_index__get_tile_extent"></a>  get_tile_extent
반환을 [익스텐트](extent-class.md) 의 값을 가진 개체를 `tiled_index` 템플릿 인수 `_Dim0`, `_Dim1`, 및 `_Dim2`합니다.  
  
## <a name="syntax"></a>구문  
  
```  
extent<rank> get_tile_extent()restrict(amp,cpu);  
```  
  
## <a name="return-value"></a>반환 값  
 `extent` 템플릿 인수 `tiled_index`, `_Dim0` 및 `_Dim1`의 값을 가진 `_Dim2` 개체입니다.  

## <a name="tiled_index__barrier"></a>  barrier   
저장소를 [tile_barrier](tile-barrier-class.md) 스레드의 현재 타일에 장애물을 나타내는 개체입니다.  
  
## <a name="syntax"></a>구문  
  
```  
const tile_barrier barrier;  
```  

## <a name="tiled_index__global"></a>  global   
저장소를 [인덱스](index-class.md) 개체는 개체의 전역 인덱스를 나타내는 차수 1, 2 또는 3입니다.  
  
## <a name="syntax"></a>구문  
  
```  
const index<rank> global;  
```  
  
## <a name="tiled_index__local"></a>  local   
저장소를 [인덱스](index-class.md) 의 현재 타일의 상대를 나타내는 차수 1, 2 또는 3 인덱스의 개체를 [tiled_extent](tiled-extent-class.md) 개체입니다.  
  
## <a name="syntax"></a>구문  
  
```  
const index<rank> local;  
```  
  
## <a name="tiled_index__rank"></a>  rank   
차수를 저장 합니다 `tiled_index` 개체입니다.  
  
## <a name="syntax"></a>구문  
  
```  
static const int rank = _Rank;  
```  

## <a name="tiled_index__tile"></a>  타일   
저장소를 [인덱스](index-class.md) 차수 1, 2 또는 3의 현재 타일의 좌표를 나타내는 개체를 [tiled_extent](tiled-extent-class.md) 개체입니다.  
  
## <a name="syntax"></a>구문  
  
```  
const index<rank> tile;  
```  
  
## <a name="tiled_index__tile_dim0"></a>  tile_dim0  
최대 유효 치수의 길이 저장 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
static const int tile_dim0 = _Dim0;  
```  
   
## <a name="tiled_index__tile_dim1"></a>  tile_dim1   
다음 최대 유효 치수의 길이 저장 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
static const int tile_dim1 = _Dim1;  
```  
## <a name="tiled_index__tile_dim2"></a>  tile_dim2   
최소 유효 치수의 길이 저장 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
static const int tile_dim2 = _Dim2;  
```  
## <a name="tiled_index__tile_origin"></a>  tile_origin   
저장소를 [인덱스](index-class.md) 개체의 현재 타일의 원점의 전역를 나타내는 차수 1, 2 또는 3 좌표를 [tiled_extent](tiled-extent-class.md) 개체입니다.  
  
## <a name="syntax"></a>구문  
  
```  
const index<rank> tile_origin  
```  
## <a name="tile_extent"></a>  tile_extent
  가져옵니다는 [익스텐트](extent-class.md) 의 값을 가진 개체를 `tiled_index` 템플릿 인수 `tiled_index` 템플릿 인수 `_Dim0`, `_Dim1`, 및 `_Dim2`합니다.  
  
## <a name="syntax"></a>구문  
  
```  
__declspec(property(get= get_tile_extent)) extent<rank> tile_extent;  
```  
  
## <a name="see-also"></a>참고 항목  
 [Concurrency 네임스페이스(C++ AMP)](concurrency-namespace-cpp-amp.md)
