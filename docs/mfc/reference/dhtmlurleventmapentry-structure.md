---
title: DHtmlUrlEventMapEntry 구조체
ms.date: 11/04/2016
f1_keywords:
- DHtmlUrlEventMapEntry
helpviewer_keywords:
- DHtmlUrlEventMapEntry structure [MFC]
ms.assetid: 43117c1f-1a51-406c-aa2f-fea647080049
ms.openlocfilehash: c9b58067a9c8b6a71cd22b654a2f82ba0f8bfe36
ms.sourcegitcommit: c3093251193944840e3d0a068ecc30e6449624ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57292655"
---
# <a name="dhtmlurleventmapentry-structure"></a>DHtmlUrlEventMapEntry 구조체

`DHtmlUrlEventMapEntry` 구조 다중 URL 이벤트 맵 지원을 제공 합니다.

## <a name="syntax"></a>구문

```
struct DHtmlUrlEventMapEntry
{
LPCTSTR szUrl;
const DHtmlEventMapEntry *pEventMap;
};
```

#### <a name="parameters"></a>매개 변수

*szUrl*<br/>
URL입니다.

*pEventMap*<br/>
URL에 연결 된 이벤트 맵입니다.

## <a name="requirements"></a>요구 사항

**헤더:** afxdhtml.h

## <a name="see-also"></a>참고자료

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)
