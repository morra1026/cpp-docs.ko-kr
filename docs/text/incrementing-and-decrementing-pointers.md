---
title: 포인터 증가 및 감소 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- incrementing pointers
- MBCS [C++], pointers
- pointers [C++], multibyte characters
- decrementing pointers
ms.assetid: 0872b4a0-e2bd-4004-8319-070efb76f2fd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: f4fff5d7ec20ce052e4d831f1556432186ebc7bb
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42603362"
---
# <a name="incrementing-and-decrementing-pointers"></a>포인터 증가 및 감소
다음 팁을 사용 합니다.  
  
-   선행 바이트, 후행 바이트가 아니라를 가리킵니다. 일반적으로 안전 후행 바이트에 대 한 포인터가 아닙니다. 것이 일반적으로 안전 역방향 보다 앞으로 문자열을 검색 합니다.  
  
-   포인터 증가/감소 함수와 한 문자씩 이동 하는 데 사용할 수 있는 매크로 가지가 있습니다.  
  
    ```  
    sz1++;  
    ```  
  
     다음과 같이 됩니다.  
  
    ```  
    sz1 = _mbsinc( sz1 );  
    ```  
  
     `_mbsinc` 하 고 `_mbsdec` 함수는 올바르게 증가 또는 감소 `character` 문자 크기와 관계 없이 단위입니다.  
  
-   감소를 다음과 같이 문자열의 헤드에 대 한 포인터가 필요합니다.  
  
    ```  
    sz2--;  
    ```  
  
     다음과 같이 됩니다.  
  
    ```  
    sz2 = _mbsdec( sz2Head, sz2 );  
    ```  
  
     문자열에 유효한 문자에 헤드 포인터 또는 수 있도록 합니다.  
  
    ```  
    sz2Head < sz2  
    ```  
  
     유효한 선행 바이트에 대 한 포인터를 해야 합니다.  
  
-   에 대 한 더 빠른 호출에 대 한 이전 문자를 가리키는 포인터를 유지 하려는 `_mbsdec`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)   
 [바이트 인덱스](../text/byte-indices.md)