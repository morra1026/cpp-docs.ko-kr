---
title: 구조체 RUNTIME_FUNCTION
ms.date: 11/04/2016
ms.assetid: 84386527-d3aa-41c5-871d-78e3e1913704
ms.openlocfilehash: 6b113f6cf1e9951f9e4578e15c9ed0af3d036fa6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50520252"
---
# <a name="struct-runtimefunction"></a>구조체 RUNTIME_FUNCTION

테이블 기반 예외 처리 스택 공간을 할당 하거나 다른 함수 (예를 들어, 리프가 아닌 함수)를 호출 하는 모든 함수에 대 한 테이블 항목을 필요 합니다. 형식이 함수 테이블 항목:

|||
|-|-|
|ULONG|함수 시작 주소|
|ULONG|함수 끝 주소|
|ULONG|정보 주소를 해제 합니다.|

RUNTIME_FUNCTION 구조 DWORD 메모리에 정렬 해야 합니다. 모든 주소는 상대 이미지, 즉, 이러한은 함수 테이블 항목을 포함 하는 이미지의 시작 주소에서 32 비트 오프셋입니다. 이러한 항목은 정렬 되며 PE32 + 이미지의.pdata 섹션에 놓여집니다. 동적으로 생성 된 함수 [JIT 컴파일러]에 대 한 이러한 기능을 지 원하는 런타임 운영 체제에이 정보를 제공할 RtlInstallFunctionTableCallback 또는 RtlAddFunctionTable를 사용 하거나 해야 합니다. 이렇게 하지 않으면 안정적이 지 않은 예외 처리 및 프로세스 디버깅 됩니다.

## <a name="see-also"></a>참고 항목

[디버거 지원, 예외 처리를 위한 해제 데이터](../build/unwind-data-for-exception-handling-debugger-support.md)