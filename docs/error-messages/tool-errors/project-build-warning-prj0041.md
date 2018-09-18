---
title: 프로젝트 빌드 경고 PRJ0041 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- PRJ0041
dev_langs:
- C++
helpviewer_keywords:
- PRJ0041
ms.assetid: dc9f4cf9-6bd5-4222-89e8-7802a59bb96b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7677c5718783065f64e52f98f7ddbed76e905d2a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46038141"
---
# <a name="project-build-warning-prj0041"></a>프로젝트 빌드 경고 PRJ0041

누락 된 찾을 수 없습니다 '종속성' file '파일에 대 한 종속성입니다. 프로젝트가 빌드할 수 있지만이 파일을 찾을 때까지 만료 표시할 계속 될 수 있습니다.

파일 (리소스 파일 또는.idl/.odl 파일 예를 들어 포함 include 문이 프로젝트 시스템에서 확인할 수 없습니다.

프로젝트 시스템에서 전처리기 문 (예: #if)를 처리 하지 않으므로 잘못 된 문이 실질적으로 빌드의 일부로 되지 않을 수 있습니다.

이 경고를 해결 하려면.rc 파일에 모든 불필요 한 코드를 삭제 하거나 적절 한 이름의 자리 표시자 파일을 추가 합니다.