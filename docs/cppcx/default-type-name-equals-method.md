---
title: '기본값:: (type_name):: Equals 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: language-reference
f1_keywords:
- VCCORLIB/Platform::Object::Equals
dev_langs:
- C++
ms.assetid: 4450f835-06fc-4758-8d0a-72cf00007873
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 36bd6e933d4e7bb1563ec6738c7ba3ed314c1cfd
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43763915"
---
# <a name="defaulttypenameequals-method"></a>default::(type_name)::Equals 메서드
지정한 개체와 현재 개체가 같은지 여부를 확인합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
  
bool Equals(  
    Object^ obj  
)  
```  
  
### <a name="parameters"></a>매개 변수  
 obj  
 비교할 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 개체가 동일하면`true` 이고, 그렇지 않으면 `false`입니다.  
  
### <a name="requirements"></a>요구 사항  
 **지원 되는 최소 클라이언트:** Windows 8  
  
 **지원 되는 최소 서버:** Windows Server 2012  
  
 **네임스페이스:** default  
  
 **헤더:** vccorlib.h  
  
## <a name="see-also"></a>참고 항목  
 [기본 네임스페이스](../cppcx/default-namespace.md)