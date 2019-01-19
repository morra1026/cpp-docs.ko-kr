---
title: 속성 맵
ms.date: 10/24/2018
helpviewer_keywords:
- OLE DB providers, properties
- maps, property
- property maps
ms.assetid: 44abde56-90ad-4612-854e-d2fa5426fa80
ms.openlocfilehash: 2d01c2f0d7fb581f9f7e93c1ec100e465a6d92f3
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556483"
---
# <a name="property-maps"></a>속성 맵

각 공급자는 세션, 행 집합 및 선택적 명령 개체 외에 하나 이상의 속성을 지원합니다. 이러한 속성은 **OLE DB 공급자 마법사**가 만든 헤더 파일의 속성 맵에 정의됩니다. 각 헤더 파일에는 그 파일에서 정의된 개체나 개체들에 대해 정의한 OLE DB 속성 그룹의 속성에 대한 맵이 있습니다. 데이터 소스 개체가 있는 헤더 파일에는 [DataSource properties](https://msdn.microsoft.com/library/ms724188)에 대한 속성 맵이 있습니다. `Session.h`에는 [Session properties](https://docs.microsoft.com/previous-versions/windows/desktop/ms714221(v=vs.85))에 대한 속성 맵이 있습니다. 행 집합 개체와 명령 개체는 *projectname*RS.h라는 단일 헤더 파일에 있습니다. 이러한 속성은 [Rowset properties](https://docs.microsoft.com/previous-versions/windows/desktop/ms711252(v=vs.85)) 그룹의 멤버입니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿 구조](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
