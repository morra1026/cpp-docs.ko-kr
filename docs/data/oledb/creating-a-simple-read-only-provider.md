---
title: 단순한 읽기 전용 공급자 만들기 | Microsoft Docs
ms.custom: ''
ms.date: 10/26/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- OLE DB providers, creating
- OLE DB provider templates, creating providers
ms.assetid: ade8ccdd-9ea4-4e46-a964-18460c2a2401
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: c8fd4e5eb25ab1e8e6b20b576a0688da7b5aa2ef
ms.sourcegitcommit: 840033ddcfab51543072604ccd5656fc6d4a5d3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50216398"
---
# <a name="creating-a-simple-read-only-provider"></a>단순한 읽기 전용 공급자 만들기

사용 하 여 OLE DB 공급자를 만든 경우는 **ATL 프로젝트 마법사** 하 고 **ATL OLE DB 공급자 마법사**를 지원 하 고 다른 기능을 추가할 수 있습니다. 공급자에 게 어떤 종류의 어떤 조건에서 소비자를 보낸다는 데이터를 검사 하 여 디자인을 시작 합니다. 특히 명령, 트랜잭션 및 기타 옵션 개체를 지원 해야 하는지 여부를 결정 하는 것이 반드시 합니다. 구현 및 테스트는 좋은 설계 치중 신속 하 게 합니다.

이 예제에서는 두 부분으로 표시 됩니다.

- 첫 번째 파트 표시 하는 방법 [간단한 읽기 전용 공급자 만들기](../../data/oledb/implementing-the-simple-read-only-provider.md) 문자열 쌍을 읽는 합니다.

- 두 번째 파트 표시 하는 방법 [단순한 읽기 전용 공급자의 향상](../../data/oledb/enhancing-the-simple-read-only-provider.md) 추가 하 여는 `IRowsetLocate` 인터페이스.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 만들기](../../data/oledb/creating-an-ole-db-provider.md)<br/>
