---
title: 컴파일러 오류 C3836 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3836
dev_langs:
- C++
helpviewer_keywords:
- C3836
ms.assetid: 254f851b-7b7d-4c34-a740-fcf72f6a636a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0a1349ff88c00f8091a8187bb963f4fb683b694e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46046032"
---
# <a name="compiler-error-c3836"></a>컴파일러 오류 C3836

정적 생성자는 멤버 이니셜라이저 목록을 사용할 수 없습니다.

관리 되는 클래스 멤버 초기화 목록도 포함 하는 정적 생성자를 사용할 수 없습니다. 정적 클래스 생성자는 클래스 초기화, 정적 데이터 멤버 초기화를 수행 하려면 공용 언어 런타임에 의해 호출 됩니다.

## <a name="example"></a>예제

다음 샘플에서는 C3836 오류가 생성 됩니다.

```
// C3836a.cpp
// compile with: /clr
ref class M
{
   static int s_i;

public:
   static M() :  s_i(1234)   // C3836, delete initializer to resolve
   {
   }
};

int main()
{
}
```
