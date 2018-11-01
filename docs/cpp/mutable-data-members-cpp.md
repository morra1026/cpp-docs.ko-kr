---
title: 변경할 수 있는 데이터 멤버 (C++)
ms.date: 11/04/2016
f1_keywords:
- mutable_cpp
helpviewer_keywords:
- mutable keyword [C++]
ms.assetid: ebe89746-3d36-43a8-8d69-f426af23f551
ms.openlocfilehash: 8d592eb97f70bfc26c075317c57ec4d5c78e3956
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50514181"
---
# <a name="mutable-data-members-c"></a>변경할 수 있는 데이터 멤버 (C++)

이 키워드는 클래스의 비정적 데이터 멤버 중에서 const가 아닌 멤버에만 적용할 수 있습니다. 데이터 멤버가 선언 된 경우 **변경할 수**에서이 데이터 멤버에 값을 할당할 수는 것을 **const** 멤버 함수입니다.

## <a name="syntax"></a>구문

```
mutable member-variable-declaration;
```

## <a name="remarks"></a>설명

예를 들어, 다음 코드는 컴파일되지 오류 없이 때문 `m_accessCount` 되도록 선언 된 **변경할 수**에서 수정할 수 있습니다 `GetFlag` 도 `GetFlag` 는 const 멤버 함수입니다.

```cpp
// mutable.cpp
class X
{
public:
   bool GetFlag() const
   {
      m_accessCount++;
      return m_flag;
   }
private:
   bool m_flag;
   mutable int m_accessCount;
};

int main()
{
}
```

## <a name="see-also"></a>참고자료

[키워드](../cpp/keywords-cpp.md)