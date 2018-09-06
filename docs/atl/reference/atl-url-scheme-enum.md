---
title: ATL_URL_SCHEME 열거형 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- ATLUTIL/ATL::ATL_URL_SCHEME
ms.assetid: f4131046-8ba0-4ec1-8209-84203f05d20e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: ee13d34bcea1e7ce2e53b0659739ee730152f287
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43755413"
---
# <a name="atlurlscheme"></a>ATL_URL_SCHEME  

이 열거형의 멤버에서 인식 하는 스키마에 대 한 상수를 제공 [CUrl](curl-class.md)합니다.

## <a name="syntax"></a>구문

```

      enum ATL_URL_SCHEME{  
   ATL_URL_SCHEME_UNKNOWN = -1,  
   ATL_URL_SCHEME_FTP     = 0,  
   ATL_URL_SCHEME_GOPHER  = 1,  
   ATL_URL_SCHEME_HTTP    = 2,  
   ATL_URL_SCHEME_HTTPS   = 3,  
   ATL_URL_SCHEME_FILE    = 4,  
   ATL_URL_SCHEME_NEWS    = 5,  
   ATL_URL_SCHEME_MAILTO  = 6,  
   ATL_URL_SCHEME_SOCKS   = 7  
};  
```

## <a name="requirements"></a>요구 사항

**헤더:** 와 atlutil.h

## <a name="see-also"></a>참고 항목

[개념](../active-template-library-atl-concepts.md)   
[CUrl::SetScheme](curl-class.md#setscheme)   
[CUrl::GetScheme](curl-class.md#getscheme)