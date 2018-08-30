---
title: 프로젝트 빌드 오류 PRJ0024 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0024
dev_langs:
- C++
helpviewer_keywords:
- PRJ0024
ms.assetid: 8bde6368-6c1b-4e04-bc5e-3c6d0b8fa1d7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: eb539a5f1ee5f1aa5f9d828d93fa6d0dc8690c22
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43215600"
---
# <a name="project-build-error-prj0024"></a>프로젝트 빌드 오류 PRJ0024

> 유니코드 경로 '*경로*' 사용자의 ANSI 코드 페이지로 변환할 수 없습니다.

*경로* 경로 문자열의 원래 유니코드 버전입니다. 경우에이 오류가 발생할 수 있는 현재 시스템 코드 페이지에 대 한 ANSI로 직접 변환할 수 없는 유니코드 경로 합니다.

이 오류는 컴퓨터에 없는 코드 페이지를 사용 하는 시스템에서 개발 된 프로젝트를 사용 하 여 작업 하는 경우에 발생할 수 있습니다.

이 오류에 대 한 해결책은 ANSI 텍스트를 사용 하거나 코드 페이지를 컴퓨터에 설치 하 고 시스템 기본값으로 설정 하도록 경로 업데이트 합니다.