---
title: 'Platform:: delegate 클래스 | Microsoft Docs'
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Delegate
dev_langs:
- C++
helpviewer_keywords:
- Platform::Delegate Class
ms.assetid: 82b21271-768f-4193-9ca2-be68ddfd546e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: bdee3e432e3482b7f1a2c6e4be4c50abb1a6bfc8
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42609588"
---
# <a name="platformdelegate-class"></a>Platform::Delegate 클래스
함수 개체를 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
public delegate void delegate_name();  
```  
  
### <a name="members"></a>멤버  
 Delegate 클래스에는 [Platform::Object Class](../cppcx/platform-object-class.md)에서 파생된 Equals(), GetHashCode() 및 ToString() 메서드가 있습니다.  
  
### <a name="remarks"></a>설명  
 [delegate](../windows/delegate-cpp-component-extensions.md) 키워드를 사용하여 대리자를 만듭니다. Platform::Delegate를 명시적으로 사용하지 마세요. 자세한 내용은 [대리자](../cppcx/delegates-c-cx.md)를 참조하세요. 만들고 대리자를 사용 하는 방법의 예제를 참조 하세요 [Creating Windows Runtime Components in c + +](/windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp)합니다.  
  
### <a name="requirements"></a>요구 사항  
 **지원 되는 최소 클라이언트:** Windows 8  
  
 **지원 되는 최소 서버:** Windows Server 2012  
  
 **네임스페이스:** Platform  
  
 **메타데이터:** platform.winmd  
  
## <a name="see-also"></a>참고 항목  
 [Platform 네임 스페이스](../cppcx/platform-namespace-c-cx.md)