---
title: 세션 개체 인터페이스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- session objects [OLE DB]
- session objects [OLE DB], interfaces
- OLE DB provider templates, object interfaces
- interfaces, session object
- interfaces, list of
ms.assetid: ac01a958-6dde-4bd7-8b63-94459e488335
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 0b88a2b04862743839b3cd438b31506c8aea0883
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50079924"
---
# <a name="session-object-interfaces"></a>세션 개체 인터페이스

다음 표에서 세션 개체에 대 한 OLE DB에서 정의 된 필수 및 선택적 인터페이스를 보여 줍니다.

|인터페이스|필수 여부|OLE DB 템플릿에서 구현 되었습니까?|
|---------------|---------------|--------------------------------------|
|[IGetDataSource](/previous-versions/windows/desktop/ms709721)|필수|예|
|[IOpenRowset](/previous-versions/windows/desktop/ms716946)|필수|예|
|[ISessionProperties](/previous-versions/windows/desktop/ms713721)|필수|예|
|[IAlterIndex](/previous-versions/windows/desktop/ms714943)|Optional|아니요|
|[IAlterTable](/previous-versions/windows/desktop/ms719764)|Optional|아니요|
|[IBindResource](/previous-versions/windows/desktop/ms714936)|Optional|아니요|
|[ICreateRow](/previous-versions/windows/desktop/ms716832)|Optional|아니요|
|[IDBCreateCommand](/previous-versions/windows/desktop/ms711625)|Optional|예|
|[IDBSchemaRowset](/previous-versions/windows/desktop/ms713686)|Optional|예|
|[IIndexDefinition](/previous-versions/windows/desktop/ms711593)|Optional|아니요|
|[ISupportErrorInfo](/previous-versions/windows/desktop/ms715816)|Optional|예|
|[ITableCreation](/previous-versions/windows/desktop/ms713639)|Optional|아니요|
|[ITableDefinition](/previous-versions/windows/desktop/ms714277)|Optional|아니요|
|[ITableDefinitionWithConstraints](/previous-versions/windows/desktop/ms720947)|Optional|아니요|
|[ITransaction](/previous-versions/windows/desktop/ms723053)|Optional|아니요|
|[ITransactionJoin](/previous-versions/windows/desktop/ms718071)|Optional|아니요|
|[ITransactionLocal](/previous-versions/windows/desktop/ms714893)|Optional|아니요|
|[ITransactionObject](/previous-versions/windows/desktop/ms713659)|Optional|아니요|

세션 개체는 행 집합 개체를 만듭니다. 공급자 명령에서는 하는 경우 세션도 명령 개체를 만듭니다 (`CCommand`를 구현 하는 OLE DB `TCommand`). 명령 개체를 구현 하는 `ICommand` 사용 하 여 인터페이스를 `ICommand::Execute` 다음 그림에 표시 된 대로 행 집합에서 명령을 실행 하는 방법입니다.

![공급자 개념적 다이어그램](../../data/oledb/media/vc4u551.gif "vc4u551")

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)