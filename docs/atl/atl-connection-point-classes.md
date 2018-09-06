---
title: ATL 연결 지점 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CFirePropNotifyEvent class, connection point classes
- connection points [C++], ATL classes
- ATL, connection points
- CComDynamicUnkArray class, connection point classes
- CFirePropNotifyEvent class
- CComUnkArray class, connection point classes
ms.assetid: 9582ba71-7ace-4df4-9c9b-1b0636953efc
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 141142db5dff185cf4f8a0ad42c4b322e7d7739a
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43763882"
---
# <a name="atl-connection-point-classes"></a>ATL 연결 지점 클래스

ATL 연결 포인트를 지원 하기 위해 다음 클래스를 사용 합니다.

- [IConnectionPointImpl](../atl/reference/iconnectionpointimpl-class.md) 연결 지점을 구현 합니다. 나타내므로 송신 인터페이스의 IID는 템플릿 매개 변수로 전달 됩니다.

- [IConnectionPointContainerImpl](../atl/reference/iconnectionpointcontainerimpl-class.md) 연결 지점 컨테이너를 관리 하 고 실행 목록 `IConnectionPointImpl` 개체입니다.

- [IPropertyNotifySinkCP](../atl/reference/ipropertynotifysinkcp-class.md) 연결 지점을 나타내는 구현 합니다 [IPropertyNotifySink](/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink) 인터페이스입니다.

- [CComDynamicUnkArray](../atl/reference/ccomdynamicunkarray-class.md) 임의 개수의 연결점 및 해당 싱크 간의 연결을 관리 합니다.

- [CComUnkArray](../atl/reference/ccomunkarray-class.md) 미리 정의 된 수의 템플릿 매개 변수로 지정 된 대로 연결을 관리 합니다.

- [CFirePropNotifyEvent](../atl/reference/cfirepropnotifyevent-class.md) 개체 속성 변경 되었거나 변경 되려고 하는 클라이언트의 싱크를에 알립니다.

- [IDispEventImpl](../atl/reference/idispeventimpl-class.md) ATL COM 개체에 대 한 연결 지점에 대 한 지원을 제공 합니다. 이러한 연결점은 COM 개체에서 제공 하는 이벤트 싱크 맵과 매핑됩니다.

- [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md) 에 적절 한 처리기 함수로 이벤트를 라우팅하도록 클래스에서 이벤트 싱크 맵과 함께 작동 합니다.

## <a name="see-also"></a>참고 항목

[연결 지점](../atl/atl-connection-points.md)

