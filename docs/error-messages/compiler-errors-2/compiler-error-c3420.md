---
title: 컴파일러 오류 C3420 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3420
dev_langs:
- C++
helpviewer_keywords:
- C3420
ms.assetid: 99b53c77-f36b-4574-9199-b53111becccb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3997bc0744bf1e1db34fe7ce1de666ebd3e3b8cd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078571"
---
# <a name="compiler-error-c3420"></a>컴파일러 오류 C3420

'finalizer': 종료자는 virtual일 수 없습니다.

종료자는 바깥쪽 형식에서 비가상으로만 호출할 수 있습니다. 따라서 가상 종료자를 선언하면 오류가 발생합니다.

자세한 내용은 [방법의 소멸자 및 종료자: 클래스 및 구조체 정의 및 사용 (C + + /cli CLI)](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3420을 생성합니다.

```
// C3420.cpp
// compile with: /clr /c
ref class R {
   virtual !R() {}   // C3420
};
```