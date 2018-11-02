---
title: 함수 형식
ms.date: 11/04/2016
ms.assetid: 7e33d5f4-dabb-406d-afb3-13777b995028
ms.openlocfilehash: 22778f3eaefa6dbcf5f85e54c0940867ef52ab72
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50526386"
---
# <a name="function-types"></a>함수 형식

두 형식의 함수는 기본적으로 합니다. 스택 프레임을 필요로 하는 함수는 프레임 함수를 라고 합니다. 스택 프레임 필요 하지 않은 함수는 리프 함수를 라고 합니다.

프레임 함수 스택 공간을 할당, 다른 함수를 호출, 비휘발성 레지스터를 저장 또는 예외 처리를 사용 하는 함수가입니다. 또한 함수 테이블 항목을 필요합니다. 프레임 함수 프롤로그와 에필로그가 필요합니다. 프레임 함수 스택 공간을 동적으로 할당 하 고 프레임 포인터를 사용할 수 있습니다. 프레임 함수에 표준 호출의 전체 기능에 있습니다.

프레임 함수가 다른 함수를 호출 하지 경우 스택의 맞출 필요는 없습니다 (단원에 언급 [스택 할당](../build/stack-allocation.md)).

리프 함수는 함수 테이블 항목 필요 하지 않습니다. 즉, 모든 함수를 호출 하거나 스택 공간을 할당할 수 없습니다는 RSP 등의 모든 비휘발성 레지스터 변경할 수 없습니다 것입니다. 실행 되는 동안 스택 정렬 되지 않은 그대로 허용 됩니다.

## <a name="see-also"></a>참고 항목

[스택 사용](../build/stack-usage.md)
