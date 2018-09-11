---
title: 컨텍스트 특성 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- attributes [C++/CLI], contexts
ms.assetid: 3086351f-77a8-4048-99e9-3b6b041b9437
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 0e3935b168220b528afaecd2e1438cfe49496b1b
ms.sourcegitcommit: f0c90000125a9497bf61e41624de189a043703c0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44313665"
---
# <a name="attribute-contexts"></a>특성 컨텍스트
네 가지 기본 필드를 사용 하 여 c + + 특성을 설명할 수 있습니다: 대상에 적용 될 수 있습니다 (**적용 대상**) 여부 반복 하는 경우 (**Repeatable**), 필요한 다른 특성이 ( **필수 특성**), 및 기타 특성을 사용 하 여 호환성 문제 (**잘못 된 특성이**). 이러한 필드는 각 특성의 참조 항목에서 해당 테이블에 나열 됩니다. 이러한 각 필드는 아래 설명 되어 있습니다.
  
## <a name="applies-to"></a>적용 대상
 이 필드는 지정된 된 특성에 대 한 법적 대상이 여러 c + + 언어 요소를 설명 합니다. 예를 들어 특성에서 "class"를 지정 하는 경우는 **적용 대상** 필드 나타냅니다 특성을 법적 c + + 클래스에만 적용 될 수 있습니다. 특성 클래스의 멤버 함수에 적용 되는 경우 구문 오류를 초래 합니다.
  
 자세한 내용은 [용도별 특성](../windows/attributes-by-usage.md)합니다.
  
## <a name="repeatable"></a>반복 가능
 이 필드는 동일한 대상에 특성을 반복적으로 적용할 수 있는지 여부를 알려 줍니다. 대부분의 특성 재현이 불가능 합니다.
  
## <a name="required-attributes"></a>필수 특성
 이 필드에 나열 되어야 하는 다른 특성 제대로 작동 하려면 지정 된 특성 (즉, 동일한 대상에 적용 됨)를 제공 합니다. 특성을이 필드에 대 한 모든 항목에 대 한 일반적인 것입니다.
  
## <a name="invalid-attributes"></a>잘못 된 특성
 이 필드는 지정된 된 특성을 사용 하 여 호환 되지 않는 다른 특성을 나열 합니다. 특성을이 필드에 대 한 모든 항목에 대 한 일반적인 것입니다.
  
## <a name="see-also"></a>참고 항목
 [C++ 특성 참조](../windows/cpp-attributes-reference.md)