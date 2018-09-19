---
title: Varargs | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: aac0c54b-0a2d-4a22-b1de-ee41381a3eb1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8305eaddf87a2e67b797bedff1944dbcbbbdbd41
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45713650"
---
# <a name="varargs"></a>Varargs

매개 변수 (예를 들어, 줄임표 인수) varargs 통해를 전달 하는 경우 기본적으로 일반 매개 변수 전달 분산이 다섯 번째 및 이후의 인수를 포함 하 여 적용 합니다. 가 다시 호출 수신자의 인수의 주소를 덤프 하 합니다. 부동 소수점 값, 정수 및 부동 소수점 레지스터를 모두 포함 됩니다 float 값 호출 수신자에 게 정수 레지스터의 값이 필요한 경우.

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)