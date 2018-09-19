---
title: 프로젝트 빌드 오류 PRJ0032 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0032
dev_langs:
- C++
helpviewer_keywords:
- PRJ0032
ms.assetid: bc6acbea-4041-4237-8b5a-f0434705d89f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 106b1c3f470bbdb134a5fd53ebaef65a4392fd4b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053578"
---
# <a name="project-build-error-prj0032"></a>프로젝트 빌드 오류 PRJ0032

프로젝트 수준의 사용자 지정 빌드 단계의 '출력' 속성이 '매크로' out 'macro_expansion' 계산 되는 포함 되어 있습니다.

프로젝트에서 사용자 지정 빌드 단계를 매크로 평가 문제 때문에 잘못 된 출력을 했습니다. 이 오류는 경로 잘못 구성 된 문자 또는 파일 경로에서 사용할 수 없는 문자 조합을 포함 하는 것을 의미할 수도 수 있습니다.

이 오류를 해결 하려면 매크로 수정 하거나 경로 지정을 수정 합니다. 확인 된 경로가 프로젝트 디렉터리의 절대 경로 보여 줍니다.