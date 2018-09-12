---
title: assert 함수에서 진단 인쇄 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
ms.assetid: 78b64200-520d-40da-9a61-71553f411d4f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1e824e94f79aa01ab3a82675fb3e8f76059c567d
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43195554"
---
# <a name="diagnostic-printed-by-the-assert-function"></a>assert 함수에서 진단 인쇄
**ANSI 4.2** **assert** 함수에 의해 인쇄되는 진단 및 해당 함수의 종료 동작  
  
**assert** 함수는 진단 메시지를 인쇄하고 식이 false(0)이면 **abort** 루틴을 호출합니다. 진단 메시지의 형식은 다음과 같습니다.  

> **Assertion failed**: <em>expression</em>**, file** <em>filename</em>**, line** *linenumber*  

여기서 *filename*은 원본 파일의 이름이며 *linenumber*는 원본 파일에서 실패한 어설션의 줄 번호입니다. *식*이 true(0이 아님)이면 어떤 작업도 수행되지 않습니다.  
  
## <a name="see-also"></a>참고 항목  
 [라이브러리 함수](../c-language/library-functions.md)