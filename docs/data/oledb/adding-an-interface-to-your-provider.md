---
title: 공급자에 인터페이스 추가 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- OLE DB provider templates, object interfaces
ms.assetid: b0fc7cf8-428a-4584-9d64-ce9074d0eb66
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 83f04b53ec7d3527ddfbd58582f435d5fb153014
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50073073"
---
# <a name="adding-an-interface-to-your-provider"></a>공급자에 인터페이스 추가

(일반적으로 데이터 원본, 행 집합, 명령 또는 세션 개체에 OLE DB 공급자 마법사에서 만든) 인터페이스를 추가 하려는 개체를 결정 합니다. 인터페이스를 추가 해야 하는 개체 공급자에서 현재 지원 하지 않는 하나는 가능성이 있습니다. ATL OLE DB 공급자 마법사 개체를 만드는 경우 실행 합니다. 클래스 뷰에서 프로젝트를 마우스 오른쪽 단추로 클릭, 클릭 **클래스 추가** 에서 합니다 **추가** 메뉴를 클릭 한 다음 **ATL OLE DB Provider**합니다. 인터페이스 코드를 별도 디렉터리에 저장 한 다음 공급자 프로젝트에 파일을 복사 하려는 경우

인터페이스를 지 원하는 새 클래스를 만든 경우 해당 클래스에서 상속 된 개체를 확인 합니다. 예를 들어, 클래스를 추가할 수 있습니다 **IRowsetIndexImpl** 행 집합 개체:

```cpp
template <class Creator>
class CAgentRowset :
    public CRowsetImpl< CAgentRowset<Creator>, CAgentMan, Creator>,
    public IRowsetIndexImpl< ... >
```

인터페이스를 추가 **COM_MAP** COM_INTERFACE_ENTRY 매크로 사용 하는 개체에 있습니다. 맵이 있는 경우 하나 만듭니다. 예를 들어:

```cpp
BEGIN_COM_MAP(CAgentRowset)
     COM_INTERFACE_ENTRY(IRowsetIndex)
END_COM_MAP()
```

행 집합 개체에 대 한 부모의 맵을 연결 개체는 부모 클래스에 위임할 수 있도록 개체입니다. 이 예제에서는 맵에 COM_INTERFACE_ENTRY_CHAIN 매크로 추가 합니다.

```cpp
BEGIN_COM_MAP(CAgentRowset)
     COM_INTERFACE_ENTRY(IRowsetIndex)
     COM_INTERFACE_ENTRY_CHAIN(CRowsetImpl)
END_COM_MAP()
```

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 템플릿을 사용하여 작업](../../data/oledb/working-with-ole-db-provider-templates.md)