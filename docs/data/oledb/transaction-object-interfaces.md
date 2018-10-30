---
title: 트랜잭션 개체 인터페이스 | Microsoft Docs
ms.custom: ''
ms.date: 10/24/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- interfaces, OLE DB
- transaction object interfaces
- OLE DB, interfaces
- OLE DB providers, transaction support
- OLE DB provider templates, object interfaces
- interfaces, list of
ms.assetid: d2ce99ce-6f7a-4ff9-bc6e-acda3633d5c8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 33aa2c3ec99db2c2581bce827425c2dfc25bb653
ms.sourcegitcommit: 840033ddcfab51543072604ccd5656fc6d4a5d3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50216307"
---
# <a name="transaction-object-interfaces"></a>트랜잭션 개체 인터페이스

트랜잭션 개체를 데이터 원본에서 작업의 원자 단위를 정의 하 고 이러한 작업 단위가 서로 관계를 결정 합니다. 이 개체는 OLE DB 공급자 템플릿에 의해 직접 지원 되지 않습니다 (즉, 사용자 고유의 개체 만들어야).

다음 표에서 OLE DB에서 트랜잭션 개체에 대해 정의 된 필수 및 선택적 인터페이스를 보여 줍니다.

|인터페이스|필수 여부|OLE DB 템플릿에서 구현 되었습니까?|
|---------------|---------------|--------------------------------------|
|[IConnectionPointContainer](/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer)|필수|아니요|
|[ITransaction](/previous-versions/windows/desktop/ms723053)|필수|아니요|
|[ISupportErrorInfo](/previous-versions/windows/desktop/ms715816)|Optional|아니요|

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
