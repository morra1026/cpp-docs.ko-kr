---
title: 문자 집합의 이점 이식성 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- character sets [C++], benefits
- portability [C++], character sets
ms.assetid: bd60b925-1498-4e4f-897b-4c8ce66edcf7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 115a4524f3b11d847291015f3bee5ca10f628310
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46423444"
---
# <a name="benefits-of-character-set-portability"></a>문자 집합 이식성의 이점

현재 않으려는 응용 프로그램을 국제화 하는 경우에 MFC 및 C 런타임 이식성 기능을 사용 하 여 얻을 수 있습니다.

- 이식 가능한 코딩은 기본 코드에 유연 합니다. 나중에 유니코드 또는 MBCS를 쉽게 이동할 수 있습니다.

- 유니코드를 사용 하면 Windows 응용 프로그램을 더 효율적입니다. Windows 유니코드를 사용 하므로 전달 되는 운영 체제에서 유니코드가 아닌 문자열 변환 과정을 거쳐야 오버 헤드를 초래 하는 합니다.


## <a name="see-also"></a>참고 항목

[유니코드 및 MBCS](../text/unicode-and-mbcs.md)<br/>
[유니코드 지원](../text/support-for-unicode.md)