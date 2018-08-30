---
title: ATL 연결 지점 예제 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- connection points [C++], examples
- examples [ATL]
ms.assetid: a49721b7-f308-43de-8868-f662a94bc81a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3a35b1e40718c26eb094eddb420f885a37907071
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43212596"
---
# <a name="atl-connection-point-example"></a>ATL 연결 지점 예제
이 예제에서는 지 원하는 개체를 보여 줍니다 [IPropertyNotifySink](/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink) 나가는 인터페이스:  
  
 [!code-cpp[NVC_ATL_Windowing#84](../atl/codesnippet/cpp/atl-connection-point-example_1.h)]  
  
 지정 하는 경우 `IPropertyNotifySink` 나가는 인터페이스와 클래스를 사용할 수 있습니다 [IPropertyNotifySinkCP](../atl/reference/ipropertynotifysinkcp-class.md) 대신 `IConnectionPointImpl`합니다. 예를 들어:  
  
 [!code-cpp[NVC_ATL_Windowing#85](../atl/codesnippet/cpp/atl-connection-point-example_2.h)]  
  
## <a name="see-also"></a>참고 항목  
 [연결 지점](../atl/atl-connection-points.md)

