---
title: 심각한 오류 C1045 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1045
dev_langs:
- C++
helpviewer_keywords:
- C1045
ms.assetid: 766c2f89-4ecd-4281-adaa-14b270cc0829
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8c18d6f9b502e818992097c3042689cf66457792
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46024777"
---
# <a name="fatal-error-c1045"></a>심각한 오류 C1045

컴파일러 한계 : 링크 사양이 너무 많이 중첩되었습니다.

중첩된 외부 참조가 컴파일러 한계를 초과했습니다. 중첩된 외부 참조는 `extern` "C++"와 같은 외부 링크 형식에서 사용할 수 있습니다. 오류를 해결하려면 중첩된 외부 참조 수를 줄입니다.