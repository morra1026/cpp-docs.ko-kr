---
title: ATL 컬렉션 및 열거자 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- enumerators, ATL classes
- collection classes, ATL
ms.assetid: 6818db73-7094-48d8-a0ca-18147beec362
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c0ff5fec4749e08826bab5572149c6cd24a204f9
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43765075"
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
|[복사 (_c)](../atl/atl-copy-policy-classes.md)|복사 정책 클래스|
|[_CopyInterface](../atl/atl-copy-policy-classes.md)|복사 정책 클래스|
|[CAdapt](../atl/reference/cadapt-class.md)|어댑터 클래스 (숨깁니다 **연산자 &** 허용 `CComPtr`합니다 `CComQIPtr`, 및 `CComBSTR` c + + 표준 라이브러리 컨테이너에 저장)|

## <a name="see-also"></a>참고 항목

[컬렉션 및 열거자](../atl/atl-collections-and-enumerators.md)

