---
title: 프로젝트 빌드 오류 PRJ0034 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0034
dev_langs:
- C++
helpviewer_keywords:
- PRJ0034
ms.assetid: 1da4a55b-231b-4476-8545-6997628fbc00
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b271875173bf0e55d94989d60a1c8f7aaf408b2a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46065584"
---
# <a name="project-build-error-prj0034"></a>프로젝트 빌드 오류 PRJ0034

프로젝트 수준의 사용자 지정에 대 한 ' 추가 종속성 ' 속성에 포함 된 단계 '매크로를' out 'macro_expansion' 계산 되는 빌드합니다.

프로젝트에서 사용자 지정 빌드 단계 추가 종속성 매크로 평가 문제 때문에 오류가 포함 되어 있습니다. 이 오류는 경로 잘못 구성 된 문자 또는 파일 경로에서 사용할 수 없는 문자 조합을 포함 하는 것을 의미할 수도 수 있습니다.

이 오류를 해결 하려면 매크로 수정 하거나 경로 지정을 수정 합니다. 확인 된 경로가 프로젝트 디렉터리의 절대 경로 보여 줍니다.