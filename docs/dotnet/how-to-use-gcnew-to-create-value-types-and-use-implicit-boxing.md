---
title: '방법: 사용 하 여 gcnew 값 형식 만들기 및 암시적 Boxing 사용'
ms.date: 11/04/2016
helpviewer_keywords:
- gcnew keyword [C++], creating value types
- boxing, implicit
- value types, creating
ms.assetid: ceb48841-d6bd-47be-a167-57f44c961603
ms.openlocfilehash: 4b7d0560d8a80d0c09e7f8d0fce83748ec1f2f28
ms.sourcegitcommit: dedd4c3cb28adec3793329018b9163ffddf890a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "57739275"
---
# <a name="how-to-use-gcnew-to-create-value-types-and-use-implicit-boxing"></a>방법: 사용 하 여 gcnew 값 형식 만들기 및 암시적 Boxing 사용

사용 하 여 [gcnew](../windows/ref-new-gcnew-cpp-component-extensions.md) 형식 다음 가비지 수집 하 여 관리 되는 힙에 배치할 수 있는 boxed 값 형식, 값에 만듭니다.

## <a name="example"></a>예제

```
// vcmcppv2_explicit_boxing4.cpp
// compile with: /clr
public value class V {
public:
   int m_i;
   V(int i) : m_i(i) {}
};

public ref struct TC {
   void do_test(V^ v) {
      if (v != nullptr)
         ;
      else
         ;
   }
};

int main() {
   V^ v = gcnew V(42);
   TC^ tc = gcnew TC;
   tc->do_test(v);
}
```

## <a name="see-also"></a>참고자료

[Boxing](../windows/boxing-cpp-component-extensions.md)
