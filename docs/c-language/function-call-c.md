---
title: 함수 호출 (C) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- function calls, C functions
- functions [C], calling
- function calls
ms.assetid: 35c66719-3f15-4d3b-97da-4e19dc97b308
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1ec4e92774cdec75e47c07407ee72444a7486f7f
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43751337"
---
# <a name="function-call-c"></a>함수 호출 (C)

‘함수 호출’은 호출되는 함수의 이름 또는 함수 포인터의 값 및 선택적으로 함수에 전달되는 인수를 포함하는 식입니다.  
  
## <a name="syntax"></a>구문

*postfix-expression*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*postfix-expression*  **(**  *argument-expression-list*<sub>opt</sub> **)**  
  
*argument-expression-list*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*assignment-expression*<br/> &nbsp;&nbsp;&nbsp;&nbsp;*argument-expression-list* **,** *assignment-expression*  
  
*postfix-expression*은 반드시 함수 식별자 또는 함수 포인터 값과 같은 함수 주소를 반드시 계산하여야 하고 *argument-expression-list*는 해당 식 목록의 값("인수")이 함수로 전달되는 식 목록(쉼표로 구분)입니다. *argument-expression-list* 인수는 비워둘 수 있습니다.  
  
함수 호출 식에는 함수 반환 값의 값과 형식이 있습니다. 함수는 배열 형식의 개체를 반환할 수 없습니다. 함수의 반환 형식이 `void`인 경우, 즉, 함수가 값을 반환하지 않도록 선언된 경우 함수 호출 식 또한 `void` 형식을 가집니다. 자세한 내용은 [함수 호출](../c-language/function-calls.md)을 참조하세요.  
  
## <a name="see-also"></a>참고 항목

[함수 호출 연산자: ()](../cpp/function-call-operator-parens.md)