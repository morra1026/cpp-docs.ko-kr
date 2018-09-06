---
title: 'Platform:: notimplementedexception 클래스 | Microsoft Docs'
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::NotImplementedException
- VCCORLIB/Platform::NotImplementedException::NotImplementedException
dev_langs:
- C++
helpviewer_keywords:
- Platform::NotImplementedException
ms.assetid: 6da26cc2-dde8-4aea-aa85-67aac55cf97b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: ee6e30b4f55b5d87ee5b1f67d39d3cc96932f065
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43760762"
---
# <a name="platformnotimplementedexception-class"></a>Platform::NotImplementedException 클래스
인터페이스 멤버가 파생된 형식으로 구현되지 않은 경우 throw됩니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
public ref class NotImplementedException : COMException,    IException,    IPrintable,    IEquatable  
```  
  
### <a name="remarks"></a>설명  
 자세한 내용은 [COMException](../cppcx/platform-comexception-class.md) 클래스를 참조하세요.  
  
### <a name="requirements"></a>요구 사항  
 **지원 되는 최소 클라이언트:** Windows 8  
  
 **지원 되는 최소 서버:** Windows Server 2012  
  
 **네임스페이스:** Platform  
  
 **메타데이터:** platform.winmd  
  
## <a name="see-also"></a>참고 항목  
 [Platform::COMException 클래스](../cppcx/platform-comexception-class.md)