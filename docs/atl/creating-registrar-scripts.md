---
title: ATL 등록자에 대 한 스크립트를 만들고 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- scripting, registry scripting
- ATL, registry
- registrar scripts [ATL]
- scripts, Registrar scripts
- scripts, creating
ms.assetid: cbd5024b-8061-4a71-be65-7fee90374a35
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: abffe3c8d0a107c48c3a14a9bf584122229ad3b7
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43767262"
---
# <a name="creating-registrar-scripts"></a>Creating Registrar Scripts

등록자 스크립트를 시스템 레지스트리에 API 기반 하는 것이 아니라 데이터 기반 액세스를 제공합니다. 데이터 기반 액세스는 레지스트리 키를 추가 하는 스크립트에 하나 이상의 줄을 소요 되므로 일반적으로 더 효율적입니다.

합니다 [ATL 컨트롤 마법사](../atl/reference/atl-control-wizard.md) COM 서버에 대 한 등록자 스크립트를 자동으로 생성 합니다. 개체와 연결 된.rgs 파일에이 스크립트를 찾을 수 있습니다.

ATL 등록자 스크립트 엔진 런타임에 등록자 스크립트를 처리합니다. ATL 서버 설치 하는 동안 스크립트 엔진을 자동으로 호출합니다.

이 문서는 등록자 스크립트와 관련 된 다음 항목을 다룹니다.

- [BNF(Backus Nauer Form) 구문 이해](../atl/understanding-backus-nauer-form-bnf-syntax.md)

- [구문 분석 트리 이해](../atl/understanding-parse-trees.md)

- [레지스트리 스크립팅 예](../atl/registry-scripting-examples.md)

- [대체 가능 매개 변수 사용(등록자 전처리기)](../atl/using-replaceable-parameters-the-registrar-s-preprocessor.md)

- [스크립트 호출](../atl/invoking-scripts.md)

## <a name="see-also"></a>참고 항목

[레지스트리 구성 요소 (등록자)](../atl/atl-registry-component-registrar.md)

