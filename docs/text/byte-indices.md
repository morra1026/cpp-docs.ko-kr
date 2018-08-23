---
title: 바이트 인덱스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MBCS [C++], byte indices
- byte indices [C++]
ms.assetid: f6e7774a-86c6-41c2-89e3-74fd46432e47
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5beb69ef7d9d3356eddef40c6bce6483079d934a
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42590802"
---
# <a name="byte-indices"></a>바이트 인덱스
다음 팁을 사용 합니다.  
  
-   포인터 조작에서 나타나는 것과 유사한 문제를 표시 하는 문자열로 바이트 단위 인덱스를 사용 합니다. 백슬래시 문자에 대 한 문자열을 검사 하는이 예제를 살펴보세요.  
  
    ```  
    while ( rgch[ i ] != '\\' )  
        i++;  
    ```  
  
     선행 바이트는 후행 바이트를 인덱스할 수 하 고 있으므로를 가리키지 않을 수 있습니다는 `character`합니다.  
  
-   사용 된 [_mbclen](../c-runtime-library/reference/mbclen-mblen-mblen-l.md) 위의 문제를 해결 하는 함수:  
  
    ```  
    while ( rgch[ i ] != '\\' )  
        i += _mbclen ( rgch + i );  
    ```  
  
     이 따라서 선행 바이트에 올바로 인덱스에 `character`합니다. `_mbclen` 함수 (1 또는 2 바이트) 문자의 크기를 결정 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)   
 [문자열의 마지막 문자](../text/last-character-in-a-string.md)