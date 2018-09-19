---
title: 컴파일러 경고 (수준 1) C4910 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
dev_langs:
- C++
helpviewer_keywords:
- C4910
ms.assetid: 67963560-fbca-4ca7-93db-06beaf7055f0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5e6db959e467ea449a66feb3ee07c202f4dee002
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46018953"
---
# <a name="compiler-warning-level-1-c4910"></a>컴파일러 경고(수준 1) C4910

'\<식별자 >': '__declspec (dllexport)' 및 'extern' 명시적 인스턴스화에서 호환 되지 않습니다.

라는 명시적 템플릿 인스턴스화가  *\<식별자 >* 모두에 의해 수정 되는 `__declspec(dllexport)` 및 `extern` 키워드입니다. 그러나 이러한 키워드는 함께 사용할 수 없습니다. `__declspec(dllexport)` 키워드는 템플릿 클래스의 인스턴스화를 의미하는 반면, `extern` 키워드는 템플릿 클래스를 자동으로 인스턴스화하지 않음을 의미합니다.

## <a name="see-also"></a>참고 항목

[명시적 인스턴스화](../../cpp/explicit-instantiation.md)<br/>
[dllexport, dllimport](../../cpp/dllexport-dllimport.md)<br/>
[일반 규칙 및 제한 사항](../../cpp/general-rules-and-limitations.md)