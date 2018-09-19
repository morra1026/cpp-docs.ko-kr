---
title: 프로젝트 빌드 오류 PRJ0031 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0031
dev_langs:
- C++
helpviewer_keywords:
- PRJ0031
ms.assetid: b42435c6-e570-4f8e-9ad5-12a7ea69ccb2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ce97e8f540295f5a2968fce22312b8e0e34cfd2a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46076894"
---
# <a name="project-build-error-prj0031"></a>프로젝트 빌드 오류 PRJ0031

사용자 지정 빌드에 대 한 '출력' 속성이 'macro_expansion' 매크로 대 한 파일에 포함 된 ' file' ' '로 확인 됨 단계입니다.

파일에서 사용자 지정 빌드 단계 매크로 평가 문제 때문에 잘못 된 출력을 했습니다. 이 오류는 경로 잘못 구성 된 문자 또는 파일 경로에서 사용할 수 없는 문자 조합을 포함 하는 것을 의미할 수도 수 있습니다.

이 오류를 해결 하려면 매크로 수정 하거나 경로 지정을 수정 합니다. 확인 된 경로가 프로젝트 디렉터리의 절대 경로 보여 줍니다.