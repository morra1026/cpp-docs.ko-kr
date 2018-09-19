---
title: 수학 오류 M6108 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- M6108
dev_langs:
- C++
helpviewer_keywords:
- M6108
ms.assetid: 054893b4-49bc-45d9-882f-7cb50ba387c0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e1624a89b472733b4adb5563c8ba52e0b03dcaa2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46048619"
---
# <a name="math-error-m6108"></a>수학 오류 M6108

제곱근

제곱근 연산의 피연산자가 음수입니다.

프로그램은 136 종료 코드로 종료 됩니다.

> [!NOTE]
>  합니다 `sqrt` FORTRAN 내장 함수 및 C 런타임 라이브러리 함수 **SQRT** 이 오류를 생성 하지 않습니다. C `sqrt` 함수는 작업을 수행 하기 전에 인수를 확인 하 고 피연산자가 음수 오류 값을 반환 합니다. 포트란 **SQRT** 함수에는 도메인 오류를 생성 합니다 [M6201](../../error-messages/tool-errors/math-error-m6201.md) 이 오류는 대신 합니다.