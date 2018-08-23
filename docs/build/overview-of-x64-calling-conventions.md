---
title: 개요 x64 호출 규칙 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a05db5eb-0844-4d9d-8b92-b1b2434be0ea
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 850ab9f4d3656391ac744f42a9f7d4b962762724
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42573378"
---
# <a name="overview-of-x64-calling-conventions"></a>x64 호출 규칙 개요
X86과 x64 간의 두 가지 중요 한 차이점은 64 비트 주소 지정 기능 및 범용 레지스터 16 64 비트의 단순 집합입니다. X64에서는 확장 된 등록 집합에 지정 된 [__fastcall](../cpp/fastcall.md) 호출 규칙 및 RISC 기반 예외 처리 모델입니다. `__fastcall` 규칙 처음 네 개의 인수 및 스택 프레임에 대 한 레지스터를 사용 하 여 추가 인수를 전달 합니다.  
  
 다음 컴파일러 옵션에는 x64에 대 한 응용 프로그램을 최적화할 수 있습니다.  
  
-   [/favor(아키텍처에 맞게 최적화)](../build/reference/favor-optimize-for-architecture-specifics.md)  
  
## <a name="calling-convention"></a>호출 규칙  
 응용 프로그램 이진 인터페이스 ABI ()에서 4 개의 등록 빠른 호출 규칙을 사용 하는 x64 기본입니다. 호출 스택의 해당 레지스터를 저장 하는 수신자에 대 한 섀도 저장소 공간 할당 됩니다. 함수 호출에 인수 및 해당 인수에 사용 되는 레지스터 간의 엄격한 일대일 대응 관계가 있습니다. 8 바이트에 맞지 않는 없거나 1, 2, 4 또는 8 바이트는 모든 인수는 참조로 전달 되어야 합니다. 여러 레지스터 단일 인수를 분산 하지가 않습니다. X87 등록 스택은 사용 되지 않습니다. 이 호출 수신자를 사용할 수 없지만 고려해 야 합니다 volatile 함수 호출에서. 모든 부동 소수점 작업은 수행할 수는 16을 사용 하 여 XMM 등록 합니다. 정수 인수는 RCX, RDX, R8 및 R9 레지스터에 전달 됩니다. 부동 소수점 인수 XMM0L, XMM1L, XMM2L, 및 XMM3L 전달 됩니다. 16 바이트 인수는 참조로 전달 됩니다. 매개 변수 전달에 자세히 설명 되어 [매개 변수 전달](../build/parameter-passing.md)합니다. 이러한 등록 하는 것 외에도 RAX, R10, R11, XMM4, 및 XMM5 volatile 간주 됩니다. 다른 모든 레지스터 volatile이 아닌 경우 등록에 자세히 설명 되어 있습니다 [사용 등록](../build/register-usage.md) 하 고 [호출자/호출 수신자 저장 레지스터](../build/caller-callee-saved-registers.md)합니다.  
  
 호출자에 게, 호출 수신자에 게 매개 변수에 대 한 공간을 할당 하는 일을 담당 이며 4 개의 등록 매개 변수를 저장 하는 데 충분 한 공간이 호출 수신자는 여러 매개 변수를 사용 하지 않습니다 하는 경우에 항상 할당 해야 합니다. Vararg C/c + + 함수와 프로토타입화 되지 않은 C 언어 함수에 대 한 지원을 간단해 집니다. Vararg 또는 프로토타입화 되지 않은 함수에 대 한 모든 부동 소수점 값을 반드시 해당 하는 범용 레지스터에 정확히 복제 되어야 합니다. 처음 4 개 이상의 매개 변수를 호출 하기 전에 처음 4 개에 대 한 섀도 저장소 위에서 스택에 저장 되어야 합니다. Vararg 함수 정보에서 확인할 수 있습니다 [Varargs](../build/varargs.md)합니다. 프로토타입화 되지 않은 함수 정보에 자세히 설명 되어 [프로토타입화 되지 않은 함수](../build/unprototyped-functions.md)합니다.  
  
## <a name="alignment"></a>맞춤  
 대부분의 구조체는 해당 자연 맞춤으로 정렬 됩니다. 기본 예외는 스택 포인터와 `malloc` 또는 `alloca` 메모리 성능을 향상 시키기 위해 16 바이트에 맞춰집니다. 16 바이트를 초과 맞춤은 수동으로 수행 해야 하지만 16 바이트 XMM 작업에 대 한 일반적인 맞춤 크기 이므로 대부분의 코드에 대 한 작동 합니다. 구조 레이아웃 및 정렬 하는 방법에 대 한 자세한 내용은 참조 하세요. [형식 및 저장소](../build/types-and-storage.md)합니다. 스택 레이아웃에 대 한 정보를 참조 하세요 [스택 사용](../build/stack-usage.md)합니다.  
  
## <a name="unwindability"></a>Unwindability  
 리프 함수는 모든 비휘발성 레지스터를 변경 하지 않는 함수입니다. 비-리프 함수는 함수를 호출 하거나 로컬 변수에 대 한 추가 스택 공간을 할당 하 여 예를 들어 비휘발성 RSP 변경할 수 있습니다. 비휘발성 레지스터를 예외로 처리 될 때 복구 하기 위해 비-리프 함수 임의의 명령에 함수를 올바르게 해제 하는 방법을 설명 하는 정적 데이터를 사용 하 여 주석을 추가 해야 합니다. 이 데이터는으로 저장 *pdata*, 또는 프로시저 데이터를 다시 참조 하는 *xdata*, 예외 데이터를 처리 합니다. xdata 해제 정보를 포함 하 고 추가 pdata 또는 예외 처리기 함수를 가리킬 수 있습니다. 프롤로그와 에필로그는 xdata에 제대로 설명 될 수 있도록 고도로 제한 합니다. 스택 포인터에 속하지 않는 프롤로그 또는 에필로그를 제외한 리프 함수 내에서 코드의 모든 지역에서 16 바이트 정렬 되어야 합니다. 리프 함수 pdata 및 xdata가 필요 하므로 반환을 시뮬레이션 하면 위치 수 있습니다. 함수 프롤로그 및 에필로그의 올바른 구조에 대 한 자세한 내용은 참조 하세요 [프롤로그 및 에필로그](../build/prolog-and-epilog.md)합니다. 예외 처리 및 예외 처리 및 pdata 및 xdata 해제 하는 방법에 대 한 자세한 내용은 참조 하십시오 [예외 처리 (x64)](../build/exception-handling-x64.md)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [x64 소프트웨어 규칙](../build/x64-software-conventions.md)