---
title: DHtmlUrlEventMapEntry 구조체
ms.date: 11/04/2016
f1_keywords:
- DHtmlUrlEventMapEntry
helpviewer_keywords:
- DHtmlUrlEventMapEntry structure [MFC]
ms.assetid: 43117c1f-1a51-406c-aa2f-fea647080049
ms.openlocfilehash: 0a1dc86080c094a7ac89940cd43a8edac973e10c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50431631"
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

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)

