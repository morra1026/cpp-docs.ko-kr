---
title: 리소스 컴파일러 심각한 오류 RC1120 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- RC1120
dev_langs:
- C++
helpviewer_keywords:
- RC1120
ms.assetid: 4e462931-e42e-42e3-8bfc-847677194286
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 62f28e381d4eac0bfd1f010ef3919452635a1b96
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46057004"
---
# <a name="resource-compiler-fatal-error-rc1120"></a>리소스 컴파일러 심각한 오류 RC1120

메모리에서 필요한 바이트 수입니다.

리소스 컴파일러는 힙에 저장 하는 항목에 대 한 저장소 부족 합니다. 일반적으로 너무 많은 기호가의 결과입니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. Windows 스왑 파일 공간을 늘립니다. 파일 스왑 공간을 늘리는 방법에 대 한 자세한 내용은 Windows 도움말에서 가상 메모리를 참조 하세요.

1. 불필요 한 제거 포함 파일, 특히 `#define`지시문과 함수 프로토타입을 합니다.

1. 현재 파일을 두 개 이상의 파일로 분할 하 고 개별적으로 컴파일할 수 있습니다.

1. 다른 프로그램 또는 많은 양의 메모리가 소비 되는 시스템에서 실행 되는 드라이버를 제거 합니다.