---
title: 트랜잭션 개체 인터페이스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
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
ms.openlocfilehash: 88b6884ff8543b3aa6ec329330563fbe1ad27b8e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46071590"
---
# <a name="transaction-object-interfaces"></a>트랜잭션 개체 인터페이스

트랜잭션 개체를 데이터 원본에서 작업의 원자 단위를 정의 하 고 이러한 작업 단위가 서로 관계를 결정 합니다. 이 개체는 OLE DB 공급자 템플릿에 의해 직접 지원 되지 않습니다 (즉, 사용자 고유의 개체 만들어야).  
  
다음 표에서 OLE DB에서 트랜잭션 개체에 대해 정의 된 필수 및 선택적 인터페이스를 보여 줍니다.  
  
|인터페이스|필수 여부|OLE DB 템플릿에서 구현 되었습니까?|  
|---------------|---------------|--------------------------------------|  
|[IConnectionPointContainer](/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer)|필수|아니요|  
|[ITransaction](/previous-versions/windows/desktop/ms723053\(v=vs.85\))|필수|아니요|  
|[ISupportErrorInfo](/previous-versions/windows/desktop/ms715816\(v=vs.85\))|Optional|아니요|  
  
## <a name="see-also"></a>참고 항목  

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)