---
title: 식 계산기 오류 CXX0065 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0065
dev_langs:
- C++
helpviewer_keywords:
- CAN0065
- CXX0065
ms.assetid: aac68f87-0b90-4c19-afa6-1c587625a5fd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c100b1edbd36f4384e8deb1abf5b36465e8da479
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46024166"
---
# <a name="expression-evaluator-error-cxx0065"></a>식 계산기 오류 CXX0065

변수 스택 프레임이 필요합니다.

식은 현재 범위 내에 존재 하지만 아직 만들지 않은 변수를 포함 합니다.

아니면 함수에 대 한 종료 코드를 한 단계씩 함수 했지만 아직 함수에 대 한 스택 프레임 설정의 프롤로그를 실행 하는 경우이 오류가 발생할 수 있습니다.

식을 계산 하기 전에 스택 프레임 설정 된 하기까지 프롤로그 코드를 단계별로 실행 합니다.

이 오류는 can0065와 동일 합니다.