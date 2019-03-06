---
title: ATL 컬렉션 및 열거자 클래스
ms.date: 11/04/2016
helpviewer_keywords:
- enumerators, ATL classes
- collection classes, ATL
ms.assetid: 6818db73-7094-48d8-a0ca-18147beec362
ms.openlocfilehash: b1ab9a160b01ea278d162a515e5121054bf398f7
ms.sourcegitcommit: c3093251193944840e3d0a068ecc30e6449624ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57265407"
---
# <a name="atl-collection-and-enumerator-classes"></a>ATL 컬렉션 및 열거자 클래스

ATL은 컬렉션 및 열거자를 구현 하는 데 다음 클래스를 제공 합니다.

|클래스|설명|
|-----------|-----------------|
|[ICollectionOnSTLImpl](../atl/reference/icollectiononstlimpl-class.md)|컬렉션 인터페이스 구현|
|[IEnumOnSTLImpl](../atl/reference/ienumonstlimpl-class.md)|열거자 인터페이스 구현 (c + + 표준 라이브러리와 호환 가능한 컨테이너에 저장 된 데이터를 가정)|
|[CComEnumImpl](../atl/reference/ccomenumimpl-class.md)|열거자 인터페이스 구현 (배열에 저장 된 데이터를 가정)|
|[CComEnumOnSTL](../atl/reference/ccomenumonstl-class.md)|열거자 개체 구현을 (사용 하 여 `IEnumOnSTLImpl`)|
|[CComEnum](../atl/reference/ccomenum-class.md)|열거자 개체 구현을 (사용 하 여 `CComEnumImpl`)|
|[_Copy](../atl/atl-copy-policy-classes.md)|복사 정책 클래스|
|[_CopyInterface](../atl/atl-copy-policy-classes.md)|복사 정책 클래스|
|[CAdapt](../atl/reference/cadapt-class.md)|어댑터 클래스 (숨깁니다 **연산자 &** 허용 `CComPtr`합니다 `CComQIPtr`, 및 `CComBSTR` c + + 표준 라이브러리 컨테이너에 저장)|

## <a name="see-also"></a>참고자료

[컬렉션 및 열거자](../atl/atl-collections-and-enumerators.md)
