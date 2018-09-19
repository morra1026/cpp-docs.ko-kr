---
title: 링커 도구 오류 LNK1188 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1188
dev_langs:
- C++
helpviewer_keywords:
- LNK1188
ms.assetid: 4af574b0-5b41-4580-9a37-52a634add995
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 36b31590d94d809c16ed64d16071db0919f60238
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46098942"
---
# <a name="linker-tools-error-lnk1188"></a>링커 도구 오류 LNK1188

BADFIXUPSECTION:: 잘못 된 픽스업 대상이 'symbol'; 가능한 길이 섹션이 0

VxD 링크 하는 동안에 재배치의 대상 섹션을 아닙니다. Link386 (이전 버전), 다른 길이가 0이 아닌 섹션을 사용 하 여 0 길이 섹션이 결합 (MASM 그룹 지시문에서 생성) OMF 그룹 레코드를 사용 합니다. GROUP 지시문 및 길이가 0 인 섹션에는 COFF 형식은 지원 하지 않습니다. 링크 자동으로이 유형의 OMF 개체를 COFF로 변환 하는 경우이 오류가 발생할 수 있습니다.