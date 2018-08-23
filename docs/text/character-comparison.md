---
title: 문자 비교 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- comparing characters
- MBCS [C++], character comparison
- characters [C++], comparing
ms.assetid: 18846e44-3e6e-40c4-9b42-3153fb15db20
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 246801abcb04cc8d9c2fd1a005183501bde240d1
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42612328"
---
# <a name="character-comparison"></a>문자 비교
다음 팁을 사용 합니다.  
  
-   올바르게 작동 ASCII 문자를 사용 하 여 알려진된 선행 바이트를 비교 합니다.  
  
    ```  
    if( *sz1 == 'A' )  
    ```  
  
-   두 개의 알 수 없는 문자를 비교 Mbstring.h에 정의 된 매크로 중 하나를 사용을 하려면 필요 합니다.  
  
    ```  
    if( !_mbccmp( sz1, sz2) )  
    ```  
  
     더블 바이트 문자의 바이트 모두 서로 같은지 비교 하는 것이 이렇게 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)   
 [버퍼 오버플로](../text/buffer-overflow.md)