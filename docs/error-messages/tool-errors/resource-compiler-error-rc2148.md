---
title: 리소스 컴파일러 오류 RC2148 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- RC2148
dev_langs:
- C++
helpviewer_keywords:
- RC2148
ms.assetid: 0290065c-35d3-4815-80c5-40bf7132ae1d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4b78bf8e9eb9ebe86dae75856ea3c0b6f5d34a26
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075909"
---
# <a name="resource-compiler-error-rc2148"></a>리소스 컴파일러 오류 RC2148

너무 많은 하위 언어 ID

보조 언어 ID 값이 범위를 벗어났습니다.

**LANGUAGE** 문에서는 다음 구문을 사용해야 합니다.

**LANGUAGE** *primary_language_ID*,*secondary_language_ID*

유효한 보조 언어 Id로 정의 됩니다 **SUBLANG_** WINNT.h 파일에는 상수입니다.