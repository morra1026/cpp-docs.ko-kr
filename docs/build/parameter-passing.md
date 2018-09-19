---
title: 매개 변수 전달 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: e838ee5f-c2fe-40b0-9a23-8023c949c820
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e8db6b61936b2122cd984e594c1ff3f162fa3dfe
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45724453"
---
# <a name="parameter-passing"></a>매개 변수 전달

처음 4 개의 정수 인수 레지스터에 전달 됩니다. 정수 값 (순서 대로 왼쪽에서 오른쪽) RCX, RDX, R8 및 R9에 전달 됩니다. 인수 5 이상이 스택에 전달 됩니다. 모든 인수가 레지스터에 오른쪽에 맞춰집니다. 이렇게 하는 경우 호출 수신자는 레지스터의 상위 비트를 무시할 수 있어야 하 고 등록 필요한 부분에만 액세스할 수 있습니다.

부동 소수점 및 이중 정밀도 인수 XMM0에 전달 됩니다-XMM3 (최대 4) 시작 하는 카디 날 슬롯에 대 한 일반적으로 사용 되는 정수 슬롯 (RCX, RDX, R8 및 R9)를 사용 하 여 무시 (예제 참조) 및 그 반대의 경우도 마찬가지입니다.

[__m128](../cpp/m128.md) 형식, 배열 및 문자열은 직접 값으로 전달 되지 않고 호출자에 의해 할당 된 메모리 포인터가 대신 전달 됩니다. 동일한 크기의 정수 처럼 크기가 8, 16, 32 또는 64 비트 및 __m64 구조체/공용 구조체 전달 됩니다. 이러한 크기 이외의 구조체/공용 구조체는 호출자가 할당 된 메모리에 대 한 포인터로 전달 됩니다. 이러한 집계 유형에 대 한 포인터로 전달 (포함 하 여 \__m128), 호출자에 게 할당 된 임시 메모리에 16 바이트 정렬 됩니다.

내장 함수에 스택 공간이 할당 하지 및 다른 함수를 호출 하지 마십시오 다른 휘발성 레지스터를 사용 하 여 컴파일러 내장 함수 구현이 사이의 긴밀 한 바인딩이 없으므로 추가 레지스터 인수를 전달할 수 있습니다. 성능 향상에 대 한 추가 기회입니다.

호출 수신자는 해당 섀도 공간이 필요한 경우에 등록 매개 변수를 덤프 해야 합니다.

다음 표에서 매개 변수를 전달 하는 방법을 보여 줍니다.

|매개 변수 형식|전달 하는 방법|
|--------------------|----------------|
|부동 소수점|처음 4 개의 매개 변수-XMM3 통해 XMM0입니다. 다른 스택에 전달 됩니다.|
|정수|처음 4 개의 매개 변수-RCX, RDX, R8 R9입니다. 다른 스택에 전달 됩니다.|
|집계 (8, 16, 32 또는 64 비트) 및 __m64|처음 4 개의 매개 변수-RCX, RDX, R8 R9입니다. 다른 스택에 전달 됩니다.|
|집계 (기타)|포인터입니다. RCX, RDX, R8 및 R9에 포인터로 전달 하는 처음 4 개의 매개 변수입니다.|
|__m128|포인터입니다. RCX, RDX, R8 및 R9에 포인터로 전달 하는 처음 4 개의 매개 변수입니다.|

## <a name="example-of-argument-passing-1---all-integers"></a>1-모든 정수를 전달 하는 인수의 예제

```
func1(int a, int b, int c, int d, int e);
// a in RCX, b in RDX, c in R8, d in R9, e pushed on stack
```

## <a name="example-of-argument-passing-2---all-floats"></a>예제 2-모든 부동 소수점 수를 전달 하는 인수

```
func2(float a, double b, float c, double d, float e);
// a in XMM0, b in XMM1, c in XMM2, d in XMM3, e pushed on stack
```

## <a name="example-of-argument-passing-3---mixed-ints-and-floats"></a>3-혼합된 정수 및 부동 소수점을 전달 하는 인수의 예제

```
func3(int a, double b, int c, float d);
// a in RCX, b in XMM1, c in R8, d in XMM3
```

## <a name="example-of-argument-passing-4--m64-m128-and-aggregates"></a>예 4를 전달 하는 인수의-__m64를 \__m128, 및 집계

```
func4(__m64 a, _m128 b, struct c, float d);
// a in RCX, ptr to b in RDX, ptr to c in R8, d in XMM3
```

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)