---
title: 컴파일러 경고(수준 1) C4376
ms.date: 11/04/2016
f1_keywords:
- C4376
helpviewer_keywords:
- C4376
ms.assetid: 5f202c74-9489-48fe-b36f-19cd882b1589
ms.openlocfilehash: b1f6e7b403931f7fe1a67974ae85001cf80eab66
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50451599"
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