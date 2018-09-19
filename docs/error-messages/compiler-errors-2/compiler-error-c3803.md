---
title: 컴파일러 오류 C3803 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3803
dev_langs:
- C++
helpviewer_keywords:
- C3803
ms.assetid: bad5fb9a-ed9a-4c15-96e7-cf06e200a50d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6a841dbaae4142e92d8e0987b0618285e4f71f60
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075868"
---
# <a name="compiler-error-c3803"></a>컴파일러 오류 C3803

'property': 속성이 해당 접근자 'accessor' 중 하나를 사용 하 여 호환 되지 않는 형식

정의 된 속성의 형식은 [속성](../../cpp/property-cpp.md) 해당 접근자 함수 중 하나에 대 한 반환 형식과 일치 하지 않습니다.

다음 샘플에서는 C3803 오류가 생성 됩니다.

```
// C3803.cpp
struct A
{
   __declspec(property(get=GetIt)) int i;
   char GetIt()
   {
      return 0;
   }

   /*
   // try the following definition instead
   int GetIt()
   {
      return 0;
   }
   */
}; // C3803

int main()
{
}
```