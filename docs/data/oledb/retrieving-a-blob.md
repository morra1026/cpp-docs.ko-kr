---
title: BLOB 검색
ms.date: 10/24/2018
helpviewer_keywords:
- retrieving BLOBs
- BLOB (binary large object), retrieving
- OLE DB, BLOBs (binary large objects)
ms.assetid: 2893eb0a-5c05-4016-8914-1e40ccbaf0b3
ms.openlocfilehash: 365b2e5636ecc65ea334730a92953070edd104ad
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50453211"
---
# <a name="retrieving-a-blob"></a>BLOB 검색

다양 한 방법으로 이진 대형 개체 (BLOB)를 검색할 수 있습니다. 사용할 수 있습니다 `DBTYPE_BYTES` 같은 인터페이스를 사용 하거나 바이트의 시퀀스로 BLOB 검색 `ISequentialStream`합니다. 자세한 내용은 [BLOB 및 OLE 개체](/previous-versions/windows/desktop/ms711511) 에 **OLE DB Programmer's Reference**합니다.

다음 코드를 사용 하 여 BLOB을 검색 하는 방법을 보여 줍니다 `ISequentialStream`합니다. 매크로 [BLOB_ENTRY](../../data/oledb/blob-entry.md) 인터페이스 및 인터페이스에 사용 되는 플래그를 지정할 수 있습니다. 테이블을 연 후 코드는 다음과 같이 호출 됩니다. `Read` 에 반복적으로 `ISequentialStream` BLOB에서 바이트를 읽을 수 있습니다. 호출 `Release` 호출 하기 전에 인터페이스 포인터를 삭제 하기 위해 `MoveNext` 다음 레코드를 가져오려고 합니다.

```cpp
class CCategories
{
public:
   ISequentialStream* pPicture;

BEGIN_COLUMN_MAP(CCategories)
   BLOB_ENTRY(4, IID_ISequentialStream, STGM_READ, pPicture)
END_COLUMN_MAP()
};
```

그런 다음 다음 코드에 의해 사용:

```cpp
CTable<CAccessor<CCategories>> categories;
ULONG cb;
BYTE myBuffer[65536];

categories.Open(session, "Categories");

while (categories.MoveNext() == S_OK)
{
   do
   {
      categories.pPicture->Read(myBuffer, 65536, &cb);
      // Do something with the buffer
   } while (cb > 0);
   categories.pPicture->Release();
}
```

BLOB 데이터를 처리 하는 매크로 대 한 자세한 내용은 참조 하세요. **열 맵 매크로** 에 [매크로 및 OLE DB 소비자 템플릿에 대 한 전역 함수](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)합니다.

## <a name="see-also"></a>참고 항목

[접근자 사용](../../data/oledb/using-accessors.md)<br/>
[OLE DB 소비자 템플릿에 대한 매크로 및 전역 함수](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)<br/>
