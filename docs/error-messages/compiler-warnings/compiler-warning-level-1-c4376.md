---
title: 컴파일러 경고 (수준 1) C4376 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4376
dev_langs:
- C++
helpviewer_keywords:
- C4376
ms.assetid: 5f202c74-9489-48fe-b36f-19cd882b1589
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1923f2aed19de5e7f438407c25640821a2fa49c2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039623"
---
# <a name="compiler-warning-level-1-c4376"></a>컴파일러 경고(수준 1) C4376

액세스 지정자 ' old_specifier:'는 지원 되지 않습니다: 사용 하십시오 ' new_specifier:' 대신

메타 데이터의 형식 및 멤버 접근성을 지정 하는 방법은 참조 하세요 [표시 유형 입력](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Type_visibility) 및 [멤버 표시 유형](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Member_visibility) 에서 [방법: 정의 사용할 클래스 및 구조체 (C + + CLI) ](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md).

## <a name="example"></a>예제

다음 샘플 C4376를 생성합니다.

```
// C4376.cpp
// compile with: /clr /W1 /c
public ref class G {
public public:   // C4376
   void m2();
};

public ref class H {
public:   // OK
   void m2();
};
```