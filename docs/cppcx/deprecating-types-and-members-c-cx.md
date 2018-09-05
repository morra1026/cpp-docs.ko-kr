---
title: 사용 중단 하는 형식 및 멤버 (C + + /cli CX) | Microsoft Docs
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: language-reference
ms.assetid: b20b01c1-a439-4ff0-8cf3-d7280c492813
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3b2f8ab1c52297a95c89f8ee00053d24baebe39d
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43764412"
---
# <a name="deprecating-types-and-members-ccx"></a>형식 및 멤버가 사용되지 않도록 지정(C++/CX)
C + + /CX를 사용 하 여 생산자와 소비자에 대 한 Windows 런타임 형식 및 멤버의 사용 중단 된 [사용 되지 않는](/uwp/api/windows.foundation.metadata.deprecatedattribute) 특성은 지원 합니다. 이 속성이 적용된 API를 사용하는 경우 API가 더 이상 사용되지 않음을 나타내고 대체 API를 사용하도록 권장하는 컴파일 타임 경고 메시지가 나타납니다. public 형식 및 메서드에서 이 특성을 적용하고 사용자 지정 메시지를 제공할 수 있습니다.  
  
> [!CAUTION]
>  합니다 [사용 되지 않는](/uwp/api/windows.foundation.metadata.deprecatedattribute) 특성은 Windows 런타임 형식에만 사용 합니다. 표준 c + + 클래스 및 멤버를 사용 하 여 [__declspec (deprecated)](../cpp/deprecated-cpp.md)합니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는 Windows 런타임 구성 요소에서 사용자 고유의 공용 API를 사용할 수 없게 하는 방법을 보여 줍니다. 형식의 두 번째 매개 변수 [Windows: Foundation:: Metadata::DeprecationType](/uwp/api/windows.foundation.metadata.deprecationtype) API가 있는지 여부를 지정 되지 않거나 제거 합니다. 현재는 DeprecationType::Deprecated 값만 지원됩니다. 특성의 세 번째 매개 변수를 지정 합니다 [Windows::Foundation::Metadata::Platform](/uwp/api/windows.foundation.metadata.platformattribute) 특성이 적용 되는 합니다.  
  
```  
  
namespace wfm = Windows::Foundation::Metadata;  
  
public ref class Bicycle sealed  
{  
  
public:  
    property double Speed;  
  
    [wfm::Deprecated("Use the Speed property to compute the angular speed of the wheel", wfm::DeprecationType::Deprecate, 0x0)]  
    double ComputeAngularVelocity();  
};  
```  
  
## <a name="supported-targets"></a>지원되는 대상  
 다음 표에서는 Deprecated 특성이 적용될 수 있는 구문을 보여 줍니다.  
  
||  
|-|  
|XAML 컨트롤|  
|대리자(delegate)|  
|이벤트(event)|  
|열거형 필드|  
|enum|  
|struct|  
|메서드|  
|클래스|  
|interface(인터페이스)|  
|속성|  
|구조체 필드|  
|매개 변수가 있는 생성자|  
  
## <a name="see-also"></a>참고 항목  
 [형식 시스템](../cppcx/type-system-c-cx.md)   
 [Visual c + + 언어 참조](../cppcx/visual-c-language-reference-c-cx.md)   
 [네임 스페이스 참조](../cppcx/namespaces-reference-c-cx.md)