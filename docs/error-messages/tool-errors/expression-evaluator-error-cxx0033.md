---
title: 식 계산기 오류 CXX0033 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0033
dev_langs:
- C++
helpviewer_keywords:
- CAN0033
- CXX0033
ms.assetid: 0bd62c5b-de89-481f-9b12-88fe84805afe
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 04f37b53c30d36a43d339132bfd9baca3e5ec70c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46057200"
---
# <a name="expression-evaluator-error-cxx0033"></a>식 계산기 오류 CXX0033

OMF 형식 정보에 오류가 있습니다.

실행 파일에 디버깅에 대 한 유효한 개체 모듈 형식 (OMF) 없었습니다.

이 오류는 can0033과 동일 합니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 실행 파일은이 버전의 Visual c + + 링커를 사용 하 여 만들어지지 않았습니다. LINK.exe의 현재 버전을 사용 하 여 개체 코드를 다시 연결 합니다.

1. .Exe 파일이 손상 되었을 수 있습니다. 다시 컴파일하고 프로그램을 다시 연결 합니다.