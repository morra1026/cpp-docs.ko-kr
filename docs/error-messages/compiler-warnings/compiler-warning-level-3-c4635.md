---
title: 컴파일러 경고 (수준 3) C4635 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4635
dev_langs:
- C++
helpviewer_keywords:
- C4635
ms.assetid: b2ba90de-c093-4a76-8076-b65878467574
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7651012d4c48d420734a9c6ec2ff051718f82007
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46038115"
---
# <a name="compiler-warning-level-3-c4635"></a>컴파일러 경고(수준 3) C4635

XML 문서 주석 대상: 잘못된 형식의 XML: 이유

컴파일러가 XML 태그에서 일부 문제를 발견했습니다.  문제를 수정하고 다시 컴파일합니다.

다음 샘플에서는 C4635를 생성합니다.

```
// C4635.cpp
// compile with: /doc /clr /W3 /c
/// <summary>
/// The contents of the folder have changed.
/// <summary/>   // C4635

// try the following line instead
// /// </summary>
public ref class Test {};
```

이 샘플은 **끝 태그 'member'가 시작 태그 'summary'와 일치하지 않습니다**를 출력합니다.

이 샘플을 사용 하 여 문제는 끝 태그를 \<요약 > 잘못 되어 컴파일러로 인식 하지 못하면는 \<요약 > 끝 태그입니다.  \<멤버 > 태그는.xdc 파일에 모든 /doc 컴파일에서 컴파일러가 포함 되어 있습니다.  따라서 여기서 문제는 끝 태그가 \</member >, 컴파일러가 처리 한 이전의 시작 태그를 일치 하지 않습니다 (\<요약 >.