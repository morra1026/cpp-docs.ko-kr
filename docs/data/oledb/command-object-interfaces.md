---
title: 명령 개체 인터페이스
ms.date: 10/24/2018
helpviewer_keywords:
- command object interfaces [C++]
- command objects [OLE DB]
- OLE DB [C++], command object interfaces
ms.assetid: dacff5ae-252c-4f20-9ad7-4e602cc48536
ms.openlocfilehash: d9f663d4e857d300e5c0f5783b86445ce824ea8e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50598876"
---
# <a name="command-object-interfaces"></a>명령 개체 인터페이스

명령 개체를 사용 하 여 `IAccessor` 매개 변수 바인딩을 지정 하는 인터페이스입니다. 소비자 호출 `IAccessor::CreateAccessor`, 배열을 전달 `DBBINDING` 구조입니다. `DBBINDING` 열 바인딩 (예: 형식 및 길이)에 대 한 정보를 포함합니다. 공급자는 구조를 받고 데이터를 전송 하는 방법 및 변환이 필요한 지 여부를 결정 합니다.

`ICommandText` 인터페이스는 텍스트 명령을 지정 하는 방법을 제공 합니다. `ICommandProperties` 명령 속성을 처리 하는 인터페이스입니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
