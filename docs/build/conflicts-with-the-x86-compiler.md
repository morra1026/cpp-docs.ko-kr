---
title: x86 컴파일러와 충돌
ms.date: 11/04/2016
ms.assetid: 8e47f0d3-afe0-42d9-9efa-de239ddd3a05
ms.openlocfilehash: e56ebc5631ac5c96a9cdd2dfc2b8e81cdeed9769
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50614268"
---
# <a name="conflicts-with-the-x86-compiler"></a>x86 컴파일러와 충돌

4 바이트 자동으로 맞추지 않습니다 스택에 x86을 사용 하는 경우 보다 더 큰 데이터 형식 컴파일러가 응용 프로그램을 컴파일합니다. 때문에 아키텍처 x86 컴파일러는 8 바이트 주소에는 4 바이트 정렬 된 스택이 예를 들어, 64 비트 정수 4 바이트 보다 큰 모든 항목을 자동으로 맞출 수 없습니다.

맞추지 않은 데이터를 사용 하 여 작업은 두 가지 의미가 있습니다.

- 정렬 된 위치에 액세스 하는 것 보다 정렬 되지 않은 위치에 액세스 하는 데 더 걸릴 수 있습니다.

- 연동된 작업에 정렬 되지 않은 위치를 사용할 수 없습니다.

더 엄격한 맞춤이 필요한 경우 사용 하 여 `__declspec(align(N)) on your variable declarations`입니다. 이 컴파일러 스택의 사양에 맞게 동적으로 정렬 하도록 합니다. 그러나 동적으로 런타임 시 스택을 조정할 응용 프로그램의 실행 속도 느려집니다 발생할 수 있습니다.

## <a name="see-also"></a>참고 항목

[형식 및 저장소](../build/types-and-storage.md)<br/>
[align](../cpp/align-cpp.md)