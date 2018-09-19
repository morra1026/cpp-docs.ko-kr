---
title: LIB 개요 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- Lib
dev_langs:
- C++
helpviewer_keywords:
- LIB [C++], modes
ms.assetid: e997d423-f574-434f-8b56-25585d137ee0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 223f5284ed25b5a13fddef879e63ec2e480f3314
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45703769"
---
# <a name="overview-of-lib"></a>LIB 개요

LIB에서 만드는 표준 라이브러리, 라이브러리, 파일 가져오기 및 내보내기에 사용할 수 [링크](../../build/reference/linker-options.md) 는 프로그램을 빌드할 때입니다. LIB 명령 프롬프트에서 실행 됩니다.

다음과 같은 모드로 LIB를 사용할 수 있습니다.

- [빌드 또는 COFF 라이브러리 수정](../../build/reference/managing-a-library.md)

- [멤버 개체를 파일에 추출합니다.](../../build/reference/extracting-a-library-member.md)

- [가져오기 라이브러리 및 내보내기 파일 만들기](../../build/reference/working-with-import-libraries-and-export-files.md)

이러한 모드는 함께 사용할 수 없습니다. LIB를 한 번에 하나의 모드 에서만 사용할 수 있습니다.

## <a name="lib-options"></a>Lib 옵션

다음 표에서 자세한 정보에 대 한 링크를 사용 하 여 lib.exe 옵션을 나열합니다.

|옵션|설명|
|-|-|
|**/ DEF**|가져오기 라이브러리 및 내보내기 파일을 만듭니다.<br/><br/>자세한 내용은 참조 [가져오기 라이브러리 및 내보내기 파일 빌드](../../build/reference/building-an-import-library-and-export-file.md)합니다.|
|**/ERRORREPORT**|   Lib.exe 사용 하 여 내부 오류에 대 한 Microsoft로 정보를 보냅니다.<br/><br/>자세한 내용은 참조 [LIB 실행](../../build/reference/running-lib.md)합니다.|
|**/EXPORT**|   프로그램에서 함수를 내보냅니다.<br/><br/>자세한 내용은 참조 [가져오기 라이브러리 및 내보내기 파일 빌드](../../build/reference/building-an-import-library-and-export-file.md)합니다.|
|**/ 추출**|   기존 라이브러리 멤버의 복사본을 포함 하는 개체 (.obj) 파일을 만듭니다.<br/><br/>자세한 내용은 참조 [라이브러리 멤버 추출](../../build/reference/extracting-a-library-member.md)합니다.|
|**/INCLUDE**|   기호를 기호 테이블에 추가합니다.<br/><br/>자세한 내용은 참조 [가져오기 라이브러리 및 내보내기 파일 빌드](../../build/reference/building-an-import-library-and-export-file.md)합니다.|
|**/LIBPATH**|   환경 라이브러리 경로를 재정의합니다.<br/><br/>자세한 내용은 참조 [라이브러리 관리](../../build/reference/managing-a-library.md)합니다.|
|**/ 목록**|   표준 출력으로 출력 라이브러리에 대 한 정보를 표시합니다.<br/><br/>자세한 내용은 참조 [라이브러리 관리](../../build/reference/managing-a-library.md)합니다.|
|**/LTCG**|   링크 타임 코드 생성을 사용 하 여 빌드될 라이브러리를 하면 됩니다.<br/><br/>자세한 내용은 참조 [LIB 실행](../../build/reference/running-lib.md)합니다.|
|**M/컴퓨터**|   프로그램에 대 한 대상 플랫폼을 지정합니다.<br/><br/>자세한 내용은 참조 [LIB 실행](../../build/reference/running-lib.md)합니다.|
|**/ 이름**|   가져오기 라이브러리를 빌드할 때 작성 중인 가져오기 라이브러리 DLL의 이름을 지정 합니다.<br/><br/>자세한 내용은 참조 [라이브러리 관리](../../build/reference/managing-a-library.md)합니다.|
|**/NODEFAULTLIB**|   외부 참조를 확인할 때 검색 하는 라이브러리 목록에서 하나 이상의 기본 라이브러리를 제거 합니다.<br/><br/>자세한 내용은 참조 [라이브러리 관리](../../build/reference/managing-a-library.md)합니다.|
|**/NOLOGO**|   LIB 저작권 메시지 및 버전 번호를 표시 하지 않습니다 하 고 명령 파일의 에코를 방지 합니다.<br/><br/>자세한 내용은 참조 [LIB 실행](../../build/reference/running-lib.md)합니다.|
|**/ 입 출력**|   기본 출력 파일 이름을 재정의합니다.<br/><br/>자세한 내용은 참조 [라이브러리 관리](../../build/reference/managing-a-library.md)합니다.|
|**/ 제거**|   출력 라이브러리에서 개체를 제거 합니다.<br/><br/>자세한 내용은 참조 [라이브러리 관리](../../build/reference/managing-a-library.md)합니다.|
|**/SUBSYSTEM**|   운영 시스템에 연결 하 여 출력 라이브러리를 생성 하는 프로그램을 실행 하는 방법을 알려줍니다.<br/><br/>자세한 내용은 참조 [라이브러리 관리](../../build/reference/managing-a-library.md)합니다.|
|**/ 자세한 정보**|   추가 하려는.obj 파일의 이름을 비롯 하 여 세션의 진행률에 대 한 세부 정보를 표시 합니다.<br/><br/>자세한 내용은 참조 [LIB 실행](../../build/reference/running-lib.md)합니다.|
|**/WX**|   경고를 오류로 처리 합니다.<br/><br/>자세한 내용은 참조 [LIB 실행](../../build/reference/running-lib.md)합니다.|

## <a name="see-also"></a>참고 항목

[LIB 참조](../../build/reference/lib-reference.md)<br/>
[LIB 입력 파일](../../build/reference/lib-input-files.md)<br/>
[LIB 출력 파일](../../build/reference/lib-output-files.md)<br/>
[기타 LIB 출력](../../build/reference/other-lib-output.md)<br/>
[라이브러리 구조](../../build/reference/structure-of-a-library.md)