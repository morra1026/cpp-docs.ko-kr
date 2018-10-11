---
title: 속성 맵 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
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
ms.openlocfilehash: 8672cca382d89eda93e624f566f754bd2eb14d0a
ms.sourcegitcommit: 3a141cf07b5411d5f1fdf6cf67c4ce928cf389c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49083413"
---
# <a name="property-maps"></a>속성 맵

세션, 행 집합 및 선택적 명령 개체 외에도 각 공급자는 하나 이상의 속성을 지원합니다. 이러한 속성은 OLE DB 공급자 마법사에서 만든 헤더 파일의 속성 맵에 정의 됩니다. 각 헤더 파일에는 개체 또는 해당 파일에 정의 된 개체에 대해 정의 된 OLE DB 속성 그룹의 속성에 대 한 맵을 포함 합니다. 데이터 원본 개체를 포함 하는 헤더 파일에 대 한 속성 맵에 포함 된 [데이터 원본 속성](https://msdn.microsoft.com/library/ms724188)합니다. Session.h에 대 한 속성 맵에 포함 된 [세션 속성](/previous-versions/windows/desktop/ms714221)합니다. 행 집합 및 명령 개체 라는 단일 헤더 파일을에 상주 *projectname*RS.h 합니다. 이러한 속성은 멤버를 [행 집합 속성](/previous-versions/windows/desktop/ms711252) 그룹입니다.  
  
## <a name="see-also"></a>참고 항목  

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)