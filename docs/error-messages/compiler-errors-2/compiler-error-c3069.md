---
title: 컴파일러 오류 C3069 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3069
dev_langs:
- C++
helpviewer_keywords:
- C3069
ms.assetid: ca94291b-2bb4-4e3f-9acf-534234b83513
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 19deba44883d7b6815d7453e4bb231043eb7c75e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078909"
---
# <a name="compiler-error-c3069"></a>컴파일러 오류 C3069

'operator': 열거형 형식에 사용할 수 없습니다.

CLR 열거형에 대해서는 연산자가 지원되지 않습니다.  자세한 내용은 [방법: C + 열거형 정의 및 사용 + CLI](../../dotnet/how-to-define-and-consume-enums-in-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3069를 생성합니다.

```
// C3069.cpp
// compile with: /clr
enum struct E { e1 };
enum F { f1 };

int main() {
   E e = E::e1;
   bool tf;
   tf = !e;   // C3069

   // supported for native enums
   F f = f1;
   tf = !f;
}
```