---
title: 컴파일러 오류 C2696 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2696
dev_langs:
- C++
helpviewer_keywords:
- C2696
ms.assetid: 6c6eb7df-1230-4346-9a73-abf14c20785d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e6e76b0c11d329c734b0609c540aca4315c7ed9f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46108744"
---
# <a name="compiler-error-c2696"></a>컴파일러 오류 C2696

'Type' 형식의 관리 되는 임시 개체를 만들 수 없습니다.

에 대 한 참조 `const` 관리 되지 않는 프로그램에서 사용 하면 컴파일러가 스택의 임시 개체를 만들고 생성자를 호출 합니다. 그러나 관리 되는 클래스를 스택에 되지 만들 수 있습니다.

C2696 사용 되지 않는 컴파일러 옵션을 사용 하 여 전용인 **/clr: oldsyntax**합니다.
