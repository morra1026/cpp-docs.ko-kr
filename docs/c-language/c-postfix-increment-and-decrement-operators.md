---
title: C 후위 증가 및 감소 연산자 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- increment operators, syntax
- scalar operators
- types [C], scalar
ms.assetid: 56ba218d-65f9-405f-8684-caccc0ca33aa
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7dc0b4c71aafe3435def0b96ae621c60ff640dc0
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43751213"
---
# <a name="c-postfix-increment-and-decrement-operators"></a>C 후위 증가 및 감소 연산자
후위 증가 및 감소 연산자의 피연산자는 수정 가능한 l-value인 스칼라 형식입니다.  
  
## <a name="syntax"></a>구문

*postfix-expression*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*postfix-expression*  **++**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*postfix-expression*  **--**

후위 증가 또는 감소 연산의 결과는 피연산자의 값입니다. 결과를 얻은 후에는 피연산자의 값이 증가 또는 감소합니다. 다음 코드에서는 후위 증가 연산자를 보여 줍니다.  
  
```  
if( var++ > 0 )  
    *p++ = *q++;  
```  
  
이 예제에서 `var` 변수는 0과 비교된 다음 증가됩니다. `var`이 증가되기 전에 양수였던 경우 다음 문이 실행됩니다. 먼저 `q`가 가리키는 개체의 값이 `p`가 가리키는 개체에 할당됩니다. 그런 다음 `q` 및 `p`가 증가됩니다.  
  
## <a name="see-also"></a>참고 항목

[후위 증가 및 감소 연산자: ++ 및 --](../cpp/postfix-increment-and-decrement-operators-increment-and-decrement.md)