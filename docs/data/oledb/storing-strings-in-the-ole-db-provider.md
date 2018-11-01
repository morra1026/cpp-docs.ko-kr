---
title: OLE DB Provider에 문자열 저장 | Microsoft Docs
ms.custom: ''
ms.date: 10/26/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- user records, editing
ms.assetid: 36cb9635-067c-4cad-8f85-962f28026f6a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 46529a97ff38071c71ecdaf93e41f3eeb405c8a6
ms.sourcegitcommit: 840033ddcfab51543072604ccd5656fc6d4a5d3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50216437"
---
# <a name="storing-strings-in-the-ole-db-provider"></a>OLE DB 공급자에 문자열 저장

MyProviderRS.h에 **ATL OLE DB 공급자 마법사** 이라는 기본 사용자 레코드를 만듭니다 `CWindowsFile`합니다. 수정 하거나 두 문자열을 처리 하려면 `CWindowsFile` 또는 다음 코드에 표시 된 대로 사용자 고유의 레코드를 추가 합니다.

```cpp
////////////////////////////////////////////////////////////////////////
class CAgentMan: 
   public WIN32_FIND_DATA
   DWORD dwBookmark;              // Add this
   TCHAR szCommand[256];          // Add this
   TCHAR szText[256];             // Add this
   TCHAR szCommand2[256];         // Add this
   TCHAR szText2[256];            // Add this
  
{
public:
BEGIN_PROVIDER_COLUMN_MAP()
   PROVIDER_COLUMN_ENTRY_STR(OLESTR("Command"), 1, 256, GUID_NULL, CAgentMan, szCommand)
   PROVIDER_COLUMN_ENTRY_STR(OLESTR("Text"), 2, 256, GUID_NULL, CAgentMan, szText) 
   PROVIDER_COLUMN_ENTRY_STR(OLESTR("Command2"), 3, 256, GUID_NULL, CAgentMan, szCommand2)
   PROVIDER_COLUMN_ENTRY_STR(OLESTR("Text2"),4, 256, GUID_NULL, CAgentMan, szText2)
END_PROVIDER_COLUMN_MAP()
   bool operator==(const CAgentMan& am) // This is optional 
   {
      return (lstrcmpi(cFileName, wf.cFileName) == 0);
   }
};
```

데이터 멤버 `szCommand` 하 고 `szText` 사용 하 여 두 문자열을 나타내는 `szCommand2` 및 `szText2` 필요한 경우 추가 열을 사용 하 여 합니다. 데이터 멤버 `dwBookmark` 이 단순한 읽기 전용 공급자에 필요 하지 않습니다 하지만 나중에 추가 하는 데 사용 되는 `IRowsetLocate` 인터페이스를 참조 하세요 [단순한 읽기 전용 공급자의 향상](../../data/oledb/enhancing-the-simple-read-only-provider.md)합니다. `==` 인스턴스를 비교 하는 연산자 (이 연산자 구현은 선택 사항).

이 완료 되 면 공급자 컴파일 및 실행을 준비 해야 합니다. 공급자를 테스트 하려면이 기능을 일치 하는 소비자가 있어야 합니다. [단순 소비자 구현](../../data/oledb/implementing-a-simple-consumer.md) 에서 테스트 소비자를 만드는 방법을 보여 줍니다. 공급자를 사용 하 여 테스트 소비자를 실행 합니다. 확인을 클릭 하면 테스트 소비자의 공급자에서 적절 한 문자열을 검색 하는 **실행할** 단추를 **소비자 테스트** 대화 상자.

공급자를 성공적으로 테스트 하는 경우에 추가 인터페이스를 구현 하 여 해당 기능을 개선 하는 것이 좋습니다. 예제에 표시 됩니다 [간단한 읽기 전용 공급자의 기능 향상](../../data/oledb/enhancing-the-simple-read-only-provider.md)합니다.

## <a name="see-also"></a>참고 항목

[단순한 읽기 전용 공급자 구현](../../data/oledb/implementing-the-simple-read-only-provider.md)<br/>
