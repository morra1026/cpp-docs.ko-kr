---
title: LINK 출력 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- link
dev_langs:
- C++
helpviewer_keywords:
- mapfiles [C++]
- ILK files
- output files [C++], linker
- files [C++], LINK
- .ilk files
- LINK tool [C++], output
- import libraries [C++], creating
- executable files [C++], as linker output
- mapfiles [C++], LINK output
- linker [C++], output files
- DLLs [C++], as linker output
- LINK tool [C++], mapfile
ms.assetid: a98b557c-1947-447a-be1f-616fb45a9580
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5ca32769d7797446dbb0766c41867da1554b037f
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706214"
---
# <a name="link-output"></a>LINK 출력

Link 출력.exe 파일, Dll, 맵 파일, 및 메시지를 포함합니다.

##  <a name="_core_output_files"></a> 출력 파일

링크에서 기본 출력 파일은.exe 파일입니다. 경우는 [/DLL](../../build/reference/dll-build-a-dll.md) 옵션을 지정 하면 링크.dll 파일을 빌드합니다. 출력 파일 이름을 사용 하 여 제어할 수 있습니다.는 [출력 파일 이름 (/out)](../../build/reference/out-output-file-name.md) 옵션입니다.

증분 모드에서는 링크 프로그램의 후속 증분 빌드에 대 한 상태 정보를 저장 하는.ilk 파일을 만듭니다. .Ilk 파일에 대 한 자세한 내용은 참조 하세요 [.ilk 파일](../../build/reference/dot-ilk-files-as-linker-input.md)합니다. 증분 링크에 대 한 자세한 내용은 참조는 [증분 링크 (/incremental)](../../build/reference/incremental-link-incrementally.md) 옵션입니다.

링크를 만들 때 포함 하는 프로그램 내보내기 (대개 DLL), 빌드에서.exp 파일을 사용한 경우가 아니면.lib 파일을 빌드합니다. 가져오기 라이브러리 파일 이름을 사용 하 여 제어할 수 있습니다.는 [/IMPLIB](../../build/reference/implib-name-import-library.md) 옵션입니다.

경우는 [맵 파일 생성 (/map)](../../build/reference/map-generate-mapfile.md) 옵션을 지정 하면 링크 맵 파일을 만듭니다.

경우는 [디버그 정보 생성 (/debug)](../../build/reference/debug-generate-debug-info.md) 옵션을 지정 하면 링크는 프로그램에 대 한 디버깅 정보를 포함 하는 PDB를 만듭니다.

##  <a name="_core_other_output"></a> 다른 출력

입력 하는 경우 `link` 다른 명령줄 입력 하지 않고 링크는 해당 옵션을 요약 usage 문을 표시 합니다.

링크 버전과 저작권 메시지를 표시 하 고 않은 경우 명령 파일 입력을 에코 합니다 [시작 배너 표시 안 함 (/ NOLOGO)](../../build/reference/nologo-suppress-startup-banner-linker.md) 옵션을 사용 합니다.

사용할 수는 [인쇄 진행 메시지 (/verbose)](../../build/reference/verbose-print-progress-messages.md) 빌드에 대 한 추가 정보를 표시 하는 옵션입니다.

링크 형식 LNK 오류 및 경고 메시지를 발급*nnnn*합니다. 이 오류 접두사 및 숫자 범위 LIB, DUMPBIN, EDITBIN로도 사용 됩니다.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)