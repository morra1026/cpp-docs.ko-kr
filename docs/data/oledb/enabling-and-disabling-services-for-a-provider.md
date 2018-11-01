---
title: 공급자 서비스 사용 및 사용 안 함
ms.date: 11/04/2016
helpviewer_keywords:
- OLE DB services [OLE DB], enabling and disabling
- service providers [OLE DB]
ms.assetid: 3deac1bb-f660-407a-92ef-95e139e280c0
ms.openlocfilehash: ca621b005dd0bad60c70298e4d49abce6fb8d1d7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50665454"
---
# <a name="enabling-and-disabling-services-for-a-provider"></a>공급자 서비스 사용 및 사용 안 함

개별 OLE DB 서비스 사용 하도록 설정 하거나 단일 공급자에 액세스 하는 모든 응용 프로그램에 대해 기본적으로 사용 하지 않도록 설정 될 수 있습니다. 사용 하 여 공급자의 CLSID에 OLEDB_SERVICES 레지스트리 항목을 추가 하 여 이렇게는 `DWORD` 다음 표에 나와 있는 것 처럼 서비스를 사용할지 여부를 지정 하는 값입니다.

|기본 서비스를 사용 하도록 설정|키워드 값|
|------------------------------|-------------------|
|모든 서비스 (기본값)|0xffffffff|
|풀링 제외한 모든 지역 및 AutoEnlistment|0xfffffffe|
|클라이언트 커서 제외한 모든 지역|0xfffffffb|
|풀링, AutoEnlistment, 및 클라이언트 커서를 제외한 모든|0xfffffff0|
|서비스가 없습니다|0x00000000|
|집계 없음, 모든 서비스 사용 안 함|\<누락 된 키 >|

## <a name="see-also"></a>참고 항목

[OLE DB 서비스 사용 및 사용 안 함](../../data/oledb/enabling-and-disabling-ole-db-services.md)