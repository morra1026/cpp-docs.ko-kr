---
title: 정수 값의 범위
ms.date: 11/04/2016
ms.assetid: 0e9c6161-8f3f-4bfb-9fcc-a6c8dc97d702
ms.openlocfilehash: bcf79877ed1bbd261a70b56d60df86adc31c897b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50632043"
---
# <a name="range-of-integer-values"></a>정수 값의 범위

**ANSI 3.1.2.5** 다양한 형식의 정수 값에 대한 표현 및 집합

정수는 32비트(4바이트)를 포함합니다. 부호 있는 정수는 2의 보수 형식으로 표시됩니다. 최상위 비트는 음수에 대해서는 부호 1을, 양수와 0에 대해서는 0을 가집니다. 값은 아래와 같습니다.

|형식|최소값 및 최대값|
|----------|-------------------------|
|**unsigned short**|0~65535|
|`signed short`|-32768 ~ 32767|
|`unsigned long`|0 ~ 4294967295|
|**signed long**|-2147483648 ~ 2147483647|

## <a name="see-also"></a>참고 항목

[정수](../c-language/integers.md)