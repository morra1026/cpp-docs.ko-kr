---
title: 프로젝트 빌드 경고 PRJ0042 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0042
dev_langs:
- C++
helpviewer_keywords:
- PRJ0042
ms.assetid: 682c9999-6f85-409f-b102-00c93243f74f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 260da8ac336c640ea875610b2c62e6c42c7d335e
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43211352"
---
# <a name="project-build-warning-prj0042"></a>프로젝트 빌드 경고 PRJ0042

> '파일에 대 한 사용자 지정 빌드 단계에 대 한 출력 속성이'*파일*' 설정 되지 않았습니다. 사용자 지정 빌드 단계를 건너뜁니다.

출력이 지정 되었기 때문에 사용자 지정 빌드 단계 실행 되지 않았습니다.

이 오류를 해결 하려면 다음을 수행 하나.

- 빌드에서 사용자 지정 빌드 단계를 제외 합니다.

- 출력을 추가 합니다.

- 사용자 지정 빌드 단계 명령의 내용을 삭제 합니다.