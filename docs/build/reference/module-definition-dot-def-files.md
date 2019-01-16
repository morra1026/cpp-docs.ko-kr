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

모듈 정의(.def) 파일은 내보내기 정보, 특성 및 링크되는 프로그램에 대한 기타 정보를 링커에 제공합니다. .def 파일은 DLL을 빌드할 때 가장 유용합니다. 모듈 정의 문 대신에 사용할 수 있는 [링커 옵션](../../build/reference/linker-options.md)이 있기 때문에 일반적으로는 .def 파일이 필요하지 않습니다. 내보내는 함수를 지정하기 위한 방법으로 [__declspec(dllexport)](../../build/exporting-from-a-dll-using-declspec-dllexport.md)을 사용할 수도 있습니다.

링커 단계에서 링커 옵션 [/DEF(모듈 정의 파일 지정)](../../build/reference/def-specify-module-definition-file.md)를 사용하여 .def 파일을 호출할 수 있습니다.

내보내기가 없는 .exe 파일을 빌드하는 경우 .def 파일을 사용하면 출력 파일의 크기가 커지고 로드 속도는 느려지게 됩니다.

예제를 보려면 [DEF 파일을 사용하여 DLL에서 내보내기](../../build/exporting-from-a-dll-using-def-files.md)를 참조하세요.

자세한 내용은 다음 단원을 참조하세요.

- [모듈 정의 문의 규칙](../../build/reference/rules-for-module-definition-statements.md)

- [EXPORTS](../../build/reference/exports.md)

- [HEAPSIZE](../../build/reference/heapsize.md)

- [LIBRARY](../../build/reference/library.md)

- [Name](../../build/reference/name-c-cpp.md)

- [SECTIONS](../../build/reference/sections-c-cpp.md)

- [STACKSIZE](../../build/reference/stacksize.md)

- [STUB](../../build/reference/stub.md)

- [VERSION](../../build/reference/version-c-cpp.md)

- [예약어](../../build/reference/reserved-words.md)

## <a name="see-also"></a>참고 항목

[C/C++ 빌드 참조](../../build/reference/c-cpp-building-reference.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)