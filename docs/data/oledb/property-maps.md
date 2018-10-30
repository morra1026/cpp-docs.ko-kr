---
title: 속성 맵 | Microsoft Docs
ms.custom: ''
ms.date: 10/24/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- OLE DB providers, properties
- maps, property
- property maps
ms.assetid: 44abde56-90ad-4612-854e-d2fa5426fa80
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 2c6c3ddc4b19cd9b65203d8a5e675b9ed75720a1
ms.sourcegitcommit: 840033ddcfab51543072604ccd5656fc6d4a5d3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50216463"
---
# <a name="property-maps"></a>속성 맵

세션, 행 집합 및 선택적 명령 개체를 사용 하 여 각 공급자는 하나 이상의 속성을 지원합니다. 이러한 속성은로 만든 헤더 파일에 저장 하는 속성 맵을 정의 합니다 **OLE DB 공급자 마법사**합니다. 각 헤더 파일에는 개체 또는 해당 파일에 정의 된 개체에 대해 정의 된 OLE DB 속성 그룹의 속성에 대 한 맵을 포함 합니다. 데이터 원본 개체를 포함 하는 헤더 파일에 대 한 속성 맵에 포함 된 [데이터 원본 속성](https://msdn.microsoft.com/library/ms724188)합니다. `Session.h` 에 대 한 속성 맵에 포함 된 [세션 속성](/previous-versions/windows/desktop/ms714221)합니다. 행 집합 및 명령 개체는 호출을 단일 헤더 파일로 *projectname*RS.h 합니다. 이러한 속성은 멤버를 [행 집합 속성](/previous-versions/windows/desktop/ms711252) 그룹입니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
