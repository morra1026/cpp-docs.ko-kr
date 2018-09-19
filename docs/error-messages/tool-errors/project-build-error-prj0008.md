---
title: 프로젝트 빌드 오류 PRJ0008 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0008
dev_langs:
- C++
helpviewer_keywords:
- PRJ0008
ms.assetid: 6bf7f17a-d2a8-4826-99c7-d600d846952f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d7c24634a845423de590228af01cb9f4779e37ab
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062789"
---
# <a name="project-build-error-prj0008"></a>프로젝트 빌드 오류 PRJ0008

'File' 파일을 삭제 하지 못했습니다.

**파일이 다른 프로세스에서 열려 있거나 쓰기 금지 되었는지 확인 합니다.**

Visual c + + 빌드에 대 한 모든 알려진된 중간 파일과 출력 파일 및 와일드 카드 사양을 충족 하는 모든 파일 삭제 또는 정리를 다시 작성 중 합니다 **정리할 때 삭제할 확장명** 속성에는 [일반 구성 설정 속성 페이지](../../ide/general-property-page-project.md)합니다.

Visual c + + 파일을 삭제할 수 없는 경우이 오류가 나타납니다. 오류를 해결 하려면 파일 및 디렉터리 쓰기 가능으로 설정 된 빌드를 수행 하는 사용자에 대 한 합니다.