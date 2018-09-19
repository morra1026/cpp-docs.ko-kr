---
title: 프로젝트 빌드 오류 PRJ0009 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0009
dev_langs:
- C++
helpviewer_keywords:
- PRJ0009
ms.assetid: 89291778-cda4-495d-983f-ddcc06dfc98b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: efeb110823e801dd86a503a7069c4898f400769e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46057186"
---
# <a name="project-build-error-prj0009"></a>프로젝트 빌드 오류 PRJ0009

빌드 로그 작성에 대 한 열 수 없습니다.

**파일이 다른 프로세스에서 열려 있거나 쓰기 금지 되었는지 확인 합니다.**

설정한 후 합니다 **빌드 로깅** 속성을 **예** 하 빌드 또는 다시 빌드를 수행 하는, Visual c + + 없습니다 단독 모드에서 빌드 로그를 열 수 있습니다.

검사는 **빌드 로깅** 열어 설정 합니다 **옵션** 대화 상자 (에 **도구** 메뉴에서 클릭 **옵션** 명령) 차례로 선택 **VC + + 빌드** 에 **프로젝트** 폴더입니다. 빌드 파일을 BuildLog.htm 이라고 하 고 중간 디렉터리 $(IntDir)에 기록 됩니다.

이 오류의 원인은 다음과 같습니다.

- Visual c + +의 두 프로세스를 실행 하 고 동시에 둘 다에서 동일한 프로젝트의 동일한 구성을 빌드하 려 시도 합니다.

- 빌드 로그 파일의 파일을 잠그는 프로세스에서 열립니다.

- 사용자 파일을 만들 수 있는 권한이 없습니다.

- 현재 사용자 BuildLog.htm 파일에 대 한 쓰기 권한이 없습니다.