---
title: 컴파일러 경고 (수준 1) C4951 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4951
dev_langs:
- C++
helpviewer_keywords:
- C4951
ms.assetid: 669d8bb7-5efa-4ba9-99db-4e65addbf054
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e26c4bc176a54f063a3f9bce2faf451a9c0406f0
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43204237"
---
# <a name="compiler-warning-level-1-c4951"></a>컴파일러 경고(수준 1) C4951

> '*함수*' 프로필 데이터가 수집 된 함수 프로필 데이터가 사용 되지 않습니다 이후 편집 되었습니다.

[/LTCG:PGUPDATE](../../build/reference/ltcg-link-time-code-generation.md)에 대한 입력 모듈에서 함수가 편집되어 이제 프로필 데이터가 유효하지 않습니다. 후 입력된 모듈이 다시 컴파일 **/ltcg: pginstrument** 함수 (*함수*)를 다른 모듈 당시에 있던 것의 제어 흐름을 사용 하 여는 **/ltcg: pginstrument**  작업 합니다.

이 경고는 정보 제공용입니다. 이 경고를 해결하려면 **/LTCG:PGINSTRUMENT**를 실행하고 모든 테스트 실행을 다시 실행한 다음 **/LTCG:PGOPTIMIZE**를 실행합니다.

**/LTCG:PGOPTIMIZE** 를 사용한 경우 이 경고는 오류로 대체됩니다.