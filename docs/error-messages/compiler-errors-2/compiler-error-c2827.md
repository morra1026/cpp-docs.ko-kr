---
title: 컴파일러 오류 C2827 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2827
dev_langs:
- C++
helpviewer_keywords:
- C2827
ms.assetid: cb3e5814-0c92-40e4-b620-98578ae3003a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 139a012f9ed4dd3b6d81d92be3c441df4f899aac
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052218"
---
# <a name="compiler-error-c2827"></a>컴파일러 오류 C2827

단항 형식을 사용 하 여 'operator o p를 전역으로 재정의할 수 없습니다.

연산자는 단항 폼 개체 외부에서 사용할 수 없습니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 개체로 로컬 오버 로드 된 연산자를 확인 합니다.

1. 적절 한 단항 연산자 오버 로드를 선택 합니다.