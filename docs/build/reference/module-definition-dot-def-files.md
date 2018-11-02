---
title: 모듈 정의(.Def) 파일
ms.date: 11/04/2016
helpviewer_keywords:
- def files
- module definition files
- .def files
ms.assetid: 08c0bc28-c5d2-47aa-9624-7fc68bcaa4d8
ms.openlocfilehash: a882d71e76b961fefb7059bee8634507f12f7986
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50460439"
---
# <a name="module-definition-def-files"></a>모듈 정의(.Def) 파일

모듈 정의 (.def) 파일 내보내기, 특성 및 연결 될 프로그램에 대 한 기타 정보에 대 한 정보를 사용 하 여 링커를 제공 합니다. .Def 파일을 DLL을 빌드할 때 가장 유용 합니다. 있기 때문에 [링커 옵션](../../build/reference/linker-options.md) 사용할 수 있는 모듈 정의 문의 대신.def 파일 일반적으로 필요 하지 않습니다. 사용할 수도 있습니다 [__declspec (dllexport)](../../build/exporting-from-a-dll-using-declspec-dllexport.md) 지정 하는 방법으로 함수를 내보냈습니다.

사용 하 여 링커 단계.def 파일을 호출할 수 있습니다 합니다 [/DEF (모듈 정의 파일 지정)](../../build/reference/def-specify-module-definition-file.md) 링커 옵션입니다.

내보내기가 없는.exe 파일을 작성 하는.def 파일을 사용 하 여 출력 파일 크고 느린 로드를 생성 됩니다.

예를 들어 참조 [DLL를 사용 하 여 DEF 파일에서 내보내는](../../build/exporting-from-a-dll-using-def-files.md)합니다.

자세한 내용은 다음 섹션을 참조 하세요.

- [모듈 정의 문의 규칙](../../build/reference/rules-for-module-definition-statements.md)

- [EXPORTS](../../build/reference/exports.md)

- [HEAPSIZE](../../build/reference/heapsize.md)

- [LIBRARY](../../build/reference/library.md)

- [이름](../../build/reference/name-c-cpp.md)

- [섹션](../../build/reference/sections-c-cpp.md)

- [STACKSIZE](../../build/reference/stacksize.md)

- [STUB](../../build/reference/stub.md)

- [버전](../../build/reference/version-c-cpp.md)

- [예약어](../../build/reference/reserved-words.md)

## <a name="see-also"></a>참고 항목

[C/C++ 빌드 참조](../../build/reference/c-cpp-building-reference.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)