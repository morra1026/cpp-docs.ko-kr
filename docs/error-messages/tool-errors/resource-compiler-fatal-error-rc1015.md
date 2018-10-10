---
title: 리소스 컴파일러 심각한 오류 RC1015 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- RC1015
dev_langs:
- C++
helpviewer_keywords:
- RC1015
ms.assetid: 23f187e1-5538-40b5-9042-edd2888f55c2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0456845152fb2879d2f58c9c40af2562c7207535
ms.sourcegitcommit: d3c41b16bf05af2149090e996d8e71cd6cd55c7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/09/2018
ms.locfileid: "48890246"
---
# <a name="resource-compiler-fatal-error-rc1015"></a>리소스 컴파일러 심각한 오류 RC1015

열기 'filename' 파일을 포함할 수 없습니다

지정 된 포함 파일, 열 수 없습니다, 없거나 찾을 수 없습니다.

환경 설정이 유효하고, 올바른 파일 경로를 지정했는지 확인합니다. 충분 한 파일 핸들은 리소스 컴파일러를 사용할 수 있는지 확인 합니다. 네트워크 드라이브에 파일이 있으면 파일을 열 권한이 있는지 확인 합니다.

RC1015는 일반 속성 페이지 -> 리소스 -> 구성 속성에서 추가 포함 디렉터리로 지정된 디렉터리에 포함 파일이 있는 경우에도 발생할 수 있습니다. 포함 파일의 전체 경로를 지정하십시오.
