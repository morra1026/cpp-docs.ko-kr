---
title: 컴파일러 한계
ms.date: 11/04/2016
helpviewer_keywords:
- cl.exe compiler, limits for language constructs
ms.assetid: f1fa59c6-55b4-414b-80c5-3df72952160d
ms.openlocfilehash: a0c6041d326982dc9807355733cf714dcfa62ca8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50600332"
---
# <a name="compiler-limits"></a>컴파일러 한계

C++ 표준에서는 다양한 언어 구문에 대한 한도를 권장합니다. 다음은 Visual C++ 컴파일러에서 권장된 한도를 구현하지 않은 경우의 목록입니다. 첫 번째 수는 ISO C++ 11 표준(INCITS/ISO/IEC 14882-2011[2012], Annex B)으로 설정된 한도이고 두 번째 수는 Visual C++로 구현된 한도입니다.

- 중첩 수준의 복합 문, 반복 제어 구조체 및 선택 제어 구조체-C++ 표준: 256, Visual C++ 컴파일러: 중첩된 문. 하지만 일반적으로 100 및 110 단계 조합에 따라 달라집니다.

- 매개 변수에서 단일 매크로 정의-C++ 표준: 256, Visual C++ 컴파일러: 127입니다.

- 단일 매크로 호출-C++ 표준의 인수: 256, Visual C++: 컴파일러 127입니다.

- (연결)-후 문자열 리터럴 또는 와이드 문자열 리터럴의 문자 C++ 표준: 65536, Visual C++ 컴파일러: NULL 종결자를 포함하여 65535 싱글바이트 문자 및 NULL 종결자를 포함하여 32767 더블 바이트 문자입니다.

- 중첩된 클래스, 구조체 또는 공용 구조체 정의 단일 수준의 `struct-declaration-list` -C++ 표준: 256, Visual C++ 컴파일러: 16입니다.	

- 멤버 이니셜라이저가 생성자 정의-C++ 표준: 6144, Visual C++ 컴파일러: 6144개 이상 있습니다.

- 범위 한정자 개수 이상의 식별자-C++ 표준: 256, Visual C++ 컴파일러: 127입니다.

- 중첩 **extern** 사양-C++ 표준: 1024, Visual C++ 컴파일러: 9(암시적 **extern**을 제외하고 전역 범위 또는 10, 암시적 개수 사양 **extern** 전역 범위에서 지정...	

- 표준 C++-템플릿 선언의 템플릿 인수: 1024, Visual C++ 컴파일러: 2046입니다.

## <a name="see-also"></a>참고자료

[비표준 동작](../cpp/nonstandard-behavior.md)
