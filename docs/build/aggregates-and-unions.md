---
title: 집계 및 공용 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- aggregates [C++], and unions
ms.assetid: 859fc211-b111-4f12-af98-de78e48f9b92
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a22fae86c48a0dcbfb43c0de79a44195945aa25a
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43223113"
---
# <a name="aggregates-and-unions"></a>집계 및 공용 구조체
배열, 구조체 및 공용 구조체와 같은 다른 형식에는 일관성 있는 집계 및 공용 구조체 저장소 및 데이터 검색을 보장 하는 보다 엄격한 맞춤 요구 사항이 있습니다. 배열, 구조체 및 공용 구조체에 대 한 정의 다음과 같습니다.  
  
 배열  
 인접 한 데이터 개체의 정렬된 된 그룹을 포함합니다. 각 개체에 요소를 라고 합니다. 모든 요소 배열 크기 및 데이터 형식이 동일한 경우  
  
 구조체  
 데이터 개체의 정렬된 된 그룹을 포함합니다. 배열의 요소와 달리 구조체 내의 데이터 개체는 다른 데이터 형식 및 크기를 가질 수 있습니다. 각 데이터 개체 구조의 멤버를 라고 합니다.  
  
 공용 구조체  
 명명 된 멤버 집합 중 하나를 포함 하는 개체입니다. 명명된 된 집합의 멤버는 모든 형식일 수 있습니다. 공용 구조체에 할당 된 저장소는 공용 구조체 맞춤에 필요한 안쪽 여백을의 가장 큰 멤버에 필요한 저장소와 동일 합니다.  
  
 다음 표에서 강력 하 게 제안 된 스칼라 구조체와 공용 구조체 멤버 맞춤을 보여 줍니다.  
  
||||  
|-|-|-|  
|스칼라 형식|C 데이터 형식|필요한 맞춤|  
|**INT8**|**char**|Byte|  
|**UINT8**|**unsigned char**|Byte|  
|**INT16**|**short**|단어|  
|**UINT16**|**unsigned short**|단어|  
|**INT32**|**int**, **long**|워드|  
|**UINT32**|**부호 없는 int, 부호 없는 long**|워드|  
|**INT64**|**__int64**|쿼드 워드|  
|**UINT64**|**unsigned __int64**|쿼드 워드|  
|**FP32 (단일 전체 자릿수)**|**float**|워드|  
|**FP64 (전체 자릿수를 두 번)**|**double**|쿼드 워드|  
|**포인터**|<strong>\*</strong>|쿼드 워드|  
|**__m64**|**struct __m64**|쿼드 워드|  
|**__m128**|**struct __m128**|Octaword|  
  
 다음 집계 맞춤 규칙이 적용 됩니다.  
  
-   맞춤 배열의 배열 요소 중 하나의 맞춤와 같습니다.  
  
-   시작 하는 구조체 또는 공용 구조체의 맞춤은 개별 멤버의 최대 맞춤. 구조체 또는 공용 구조체 내에서 각 멤버는 이전 멤버에 따라 암시적 내부 채우기 필요할 수 있는 이전 테이블에 정의 된 대로 적절 한 맞춤에 배치 되어야 합니다.  
  
-   구조체의 크기가 후 마지막 멤버는 해당 맞춤의 배수가 이어야 합니다. 구조체 및 공용 구조체 배열에 그룹화 할 수 있습니다, 되므로 구조체 또는 공용 구조체의 각 배열 요소 시작 하 고 이전에 결정 하는 적절 한 맞춤에 종료 해야 합니다.  
  
-   보다 커야 맞춤 요구 사항으로 위의 규칙을 준수 하는 방식에 대 한 데이터를 정렬 하는 것이 가능 합니다.  
  
-   개별 컴파일러 크기 이유로 구조체의 압축을 조정할 수 있습니다. 예를 들어 [/Zp (구조체 멤버 맞춤)](../build/reference/zp-struct-member-alignment.md) 구조체의 압축을 조정할 수 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [형식 및 저장소](../build/types-and-storage.md)
