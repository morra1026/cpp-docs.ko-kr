---
title: 스칼라 형식
ms.date: 11/04/2016
ms.assetid: 07c9195e-b6c7-4083-8ef0-8a93032e4d1e
ms.openlocfilehash: 0c2fa18022763564a29b6a96f8ce719039dcd216
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50492067"
---
# <a name="scalar-types"></a>스칼라 형식

데이터에 대 한 액세스는 모든 맞춤에서 발생할 수 있습니다, 있지만 데이터 성능 손실 (또는 그 배수)를 방지 하려면 원래 경계에 정렬 하는 것이 좋습니다. 열거형 상수 정수 되며 32 비트 정수로 처리 됩니다. 다음 표에 형식 정 및 권장 되는 저장소에 대 한 맞춤 값을 사용 하 여 맞춤 관련이 있으므로:

- 바이트-8 비트

- Word-16 비트

- 2 배 워드-32 비트

- 쿼드 Word-64 비트

- 옥 타 Word-128 비트

|||||
|-|-|-|-|
|스칼라 형식|C 데이터 형식|저장소 크기 (바이트)|권장 되는 맞춤|
|**INT8**|**char**|1|Byte|
|**UINT8**|**unsigned char**|1|Byte|
|**INT16**|**short**|2|단어|
|**UINT16**|**unsigned short**|2|단어|
|**INT32**|**int**, **long**|4|워드|
|**UINT32**|**부호 없는 int, 부호 없는 long**|4|워드|
|**INT64**|**__int64**|8|쿼드 워드|
|**UINT64**|**unsigned __int64**|8|쿼드 워드|
|**FP32 (단일 전체 자릿수)**|**float**|4|워드|
|**FP64 (전체 자릿수를 두 번)**|**double**|8|쿼드 워드|
|**포인터**|<strong>\*</strong>|8|쿼드 워드|
|**__m64**|**struct __m64**|8|쿼드 워드|
|**__m128**|**struct __m128**|16|Octaword|

## <a name="see-also"></a>참고 항목

[형식 및 저장소](../build/types-and-storage.md)