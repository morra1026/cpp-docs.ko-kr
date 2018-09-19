---
title: 컴파일러 오류 C2657 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2657
dev_langs:
- C++
helpviewer_keywords:
- C2657
ms.assetid: f7cf29a9-684a-4605-9469-ecfee9ba4b03
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 342b336582b7920756a17b99f0d52dcb28c7173a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46109979"
---
# <a name="compiler-error-c2657"></a>컴파일러 오류 C2657

' 클래스:: *' 문의 시작 위치 (형식을 지정 하려면 했는지?)

줄은 포인터 멤버 식별자를 사용 하 여 시작 합니다.

이 오류는 멤버에 대 한 포인터의 선언에 누락 된 형식 지정자에서 발생할 수 있습니다.

다음 샘플에서는 C2657 오류가 생성 됩니다.

```
// C2657.cpp
class C {};
int main() {
   C::* pmc1;        // C2657
   int C::* pmc2;   // OK
}
```