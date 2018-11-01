---
title: 예약어
ms.date: 11/04/2016
f1_keywords:
- code
- CONFORMING
- DISCARDABLE
- Description
- base
- APPLOADER
- Data
- DYNAMIC
- DEV386
helpviewer_keywords:
- .def files [C++], reserved words
- def files [C++], reserved words
- linker [C++], reserved words
- reserved words [C++]
ms.assetid: 9b9f49e5-0739-45ab-a37e-81e3915ceb25
ms.openlocfilehash: 360baf479f9100483fe694ca8860dfc1d7ebfe11
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50502468"
---
# <a name="reserved-words"></a>예약어

링커에 의해에서는 다음 단어가 예약 되어 있습니다. 이러한 이름은의 인수로 사용할 수 있습니다 [모듈 정의 문의](../../build/reference/module-definition-dot-def-files.md) 이름을 큰따옴표로 묶은 경우에 ("").

||||
|-|-|-|
|**APPLOADER**<sup>1</sup>|**INITINSTANCE**<sup>2</sup>|**미리 로드**|
|**자료**|**IOPL**|**개인**|
|**코드**|**라이브러리**<sup>1</sup>|**PROTMODE**<sup>2</sup>|
|**준수**|**LOADONCALL**<sup>1</sup>|**순수**<sup>1</sup>|
|**데이터**|**LONGNAMES**<sup>2</sup>|**읽기 전용**|
|**설명**|**이동 가능한**<sup>1</sup>|**READWRITE**|
|**DEV386**|**MOVEABLE**<sup>1</sup>|**REALMODE**<sup>1</sup>|
|**무시할 수**|**여러**|**상주**|
|**동적**|**이름**|**RESIDENTNAME**<sup>1</sup>|
|**실행 전용**|**NEWFILES**<sup>2</sup>|**섹션**|
|**EXECUTEONLY**|**NODATA**<sup>1</sup>|**세그먼트**|
|**실행 읽기**|**NOIOPL**<sup>1</sup>|**공유**|
|**EXETYPE**|**NONAME**|**단일**|
|**EXPORTS**|**표준에 맞지 않는**<sup>1</sup>|**STACKSIZE**|
|**고정**<sup>1</sup>|**NONDISCARDABLE**|**STUB**|
|**함수**<sup>2</sup>|**없음**|**버전**|
|**HEAPSIZE**|**비공유**|**WINDOWAPI**|
|**가져오기**|**NOTWINDOWCOMPAT**<sup>1</sup>|**WINDOWCOMPAT**|
|**비 순수형**<sup>1</sup>|**개체**|**WINDOWS**|
|**포함**<sup>2</sup>|**이전**<sup>1</sup>||

<sup>1</sup> 링커가이 용어를 발견할 때 경고 ("무시")을 내보냅니다. 그러나 단어 여전히 예약 되어 있습니다.

<sup>2</sup> 링커가이 단어를 무시 하지만 없는 경고를 생성 합니다.

## <a name="see-also"></a>참고자료

- [링커 옵션 설정](../../build/reference/setting-linker-options.md)
- [링커 옵션](../../build/reference/linker-options.md)