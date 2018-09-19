---
title: 컴파일러 오류 C2775 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2775
dev_langs:
- C++
helpviewer_keywords:
- C2775
ms.assetid: 9c488508-ade0-48f1-b94f-d538d15f807a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4c5a3031fede7b2f47510f80eba09f62a06343f7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045837"
---
# <a name="compiler-error-c2775"></a>컴파일러 오류 C2775

'identifier': 없음 'get' 메서드는이 속성을 사용 하 여 연결

데이터 멤버를 사용 하 여 선언 합니다 [속성](../../cpp/property-cpp.md) 확장된 특성이 없으면를 `get` 함수를 지정 했지만 식을 해당 값을 검색 하려고 합니다.

다음 샘플에서는 C2775 오류가 생성 됩니다.

```
// C2775.cpp
struct A {
   __declspec(property(put=PutProp2, get=GetProp2)) int prop2;
   int GetProp2(){return 0;}
   void PutProp2(int){}

   __declspec(property(put=PutProp)) int prop;
   int PutProp(void){}

};

int main() {
   A* pa = new A;
   int x;
   x = pa->prop;   // C2775
   x = pa->prop2;
}
```