---
title: 문자 집합 이식성의 이점
ms.date: 11/04/2016
helpviewer_keywords:
- character sets [C++], benefits
- portability [C++], character sets
ms.assetid: bd60b925-1498-4e4f-897b-4c8ce66edcf7
ms.openlocfilehash: 446d59fe62999e5be652be5efabb53fd907fcd88
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50631351"
---
# <a name="benefits-of-character-set-portability"></a>문자 집합 이식성의 이점

지금 개발중인 응용 프로그램에 바로 국제화 전략을 고민하지 않는다고 하더라도, MFC 및 C 런타임의 이식성 기능을 사용하면 좋은 이유가 있습니다.

- 이식 가능한 코딩은 코드 기반을 유연하게 만들어 나중에 유니코드 또는 MBCS를 쉽게 선택할 수 있습니다.

- 유니코드를 사용한 Windows 응용 프로그램의 동작 그렇지 않은 프로그램보다 효율적입니다. Windows 유니코드를 사용 하므로 운영체제에서 주고받은 유니코드가 아닌 문자열을 변환하는 오버 헤드가 발생합니다.

## <a name="see-also"></a>참고 항목

[유니코드 및 MBCS](../text/unicode-and-mbcs.md)<br/>
[유니코드 지원](../text/support-for-unicode.md)
