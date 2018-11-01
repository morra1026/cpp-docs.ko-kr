---
title: 프로젝트 빌드 오류 PRJ0008
ms.date: 11/04/2016
f1_keywords:
- PRJ0008
helpviewer_keywords:
- PRJ0008
ms.assetid: 6bf7f17a-d2a8-4826-99c7-d600d846952f
ms.openlocfilehash: 696b77e9906b231a680027a3faaf23e53d8fb6e9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50525907"
---
# <a name="project-build-error-prj0008"></a>프로젝트 빌드 오류 PRJ0008

'File' 파일을 삭제 하지 못했습니다.

**파일이 다른 프로세스에서 열려 있거나 쓰기 금지 되었는지 확인 합니다.**

Visual c + + 빌드에 대 한 모든 알려진된 중간 파일과 출력 파일 및 와일드 카드 사양을 충족 하는 모든 파일 삭제 또는 정리를 다시 작성 중 합니다 **정리할 때 삭제할 확장명** 속성에는 [일반 구성 설정 속성 페이지](../../ide/general-property-page-project.md)합니다.

Visual c + + 파일을 삭제할 수 없는 경우이 오류가 나타납니다. 오류를 해결 하려면 파일 및 디렉터리 쓰기 가능으로 설정 된 빌드를 수행 하는 사용자에 대 한 합니다.