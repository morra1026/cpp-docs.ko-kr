---
title: . 링커 입력 파일로 ilk 파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- ILK files
- .ilk files
ms.assetid: 7324c104-9e5d-423d-b268-b59f92607bf2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f3b8de3758daf59a543cdcc9f3b73e1d6c6f0ce8
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45720592"
---
# <a name="ilk-files-as-linker-input"></a>링커 입력 파일로 사용하는 .Ilk 파일

증분 방식으로 연결 하는 경우 링크의 첫 번째 증분 링크 중에 만든.ilk 상태 파일을 업데이트 합니다. 이 파일은.exe 파일 또는.dll 파일과 동일한 기본 이름을 있고 확장.ilk 합니다. 후속 증분 링크 하는 동안 링크.ilk 파일을 업데이트 합니다. .Ilk 파일이 없는 경우 링크는 전체 링크를 수행 하 고 새.ilk 파일을 만듭니다. .Ilk 파일에 사용할 수 없는 경우 비증분 링크를 수행 합니다. 증분 링크에 대 한 자세한 내용은 참조는 [증분 링크 (/incremental)](../../build/reference/incremental-link-incrementally.md) 옵션입니다.

## <a name="see-also"></a>참고 항목

[LINK 입력 파일](../../build/reference/link-input-files.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)