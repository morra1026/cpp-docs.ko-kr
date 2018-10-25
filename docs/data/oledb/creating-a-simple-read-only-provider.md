---
title: 단순한 읽기 전용 공급자 만들기 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
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
ms.openlocfilehash: b32517e8254f383e624c5262f3a806e66ed28824
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50056258"
---
# <a name="creating-a-simple-read-only-provider"></a>단순한 읽기 전용 공급자 만들기

ATL 프로젝트 마법사 및 ATL OLE DB 공급자 마법사를 사용 하 여 OLE DB 공급자를 만들면 지원 하 고 다른 기능을 추가할 수 있습니다. 공급자에 게 보낼 상황 및 소비자에 게 데이터의 종류를 검사 하 여 디자인을 시작 합니다. 특히 명령, 트랜잭션 및 기타 옵션 개체를 지원 해야 하는지 여부를 결정 하는 것이 반드시 합니다. 구현 및 테스트는 좋은 설계 치중 신속 하 게 합니다.

이 예제에서는 두 부분으로 표시 됩니다.

- 첫 번째 파트 표시 하는 방법 [간단한 읽기 전용 공급자 만들기](../../data/oledb/implementing-the-simple-read-only-provider.md) 문자열 쌍을 읽는 합니다.

- 두 번째 파트 표시 하는 방법 [단순한 읽기 전용 공급자의 향상](../../data/oledb/enhancing-the-simple-read-only-provider.md) 추가 하 여는 `IRowsetLocate` 인터페이스.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 만들기](../../data/oledb/creating-an-ole-db-provider.md)