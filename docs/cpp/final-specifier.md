---
title: final 지정자
ms.date: 11/04/2016
f1_keywords:
- final_CPP
helpviewer_keywords:
- final Identifier
ms.assetid: 649866d0-79d4-449f-ab74-f84b911b79a3
ms.openlocfilehash: c6400c8060664713fdd004a5aa9536e0617bc0c8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50588086"
---
# <a name="final-specifier"></a>final 지정자

사용할 수는 **최종** 파생된 클래스에서 재정의할 수 없는 가상 함수를 지정 하는 키워드입니다. 상속할 수 없는 클래스를 지정하기 위해 해당 키워드를 사용할 수도 있습니다.

## <a name="syntax"></a>구문

```
function-declaration final;
class class-name final base-classes
```

## <a name="remarks"></a>설명

**최종** 상황에 맞는 이며 이름 이거나 클래스 또는 함수 선언 후에 사용 될, 경우에 예약된 된 키워드에만 특별 한 의미가 있습니다.

때 **최종** 클래스 선언에는 `base-classes` 는 선언의 선택적 부분입니다.

## <a name="example"></a>예제

다음 예제에서는 합니다 **최종** 키워드를 지정 하는 가상 함수를 재정의할 수 없습니다.

```cpp
class BaseClass
{
    virtual void func() final;
};

class DerivedClass: public BaseClass
{
    virtual void func(); // compiler error: attempting to
                         // override a final function
};
```

멤버 함수를 재정의할 수 있음을 지정 하는 방법에 대 한 정보를 참조 하세요 [재정의 지정자](../cpp/override-specifier.md)합니다.

다음 예제에서는 합니다 **최종** 키워드를 지정 된 클래스를 상속할 수 없습니다.

```cpp
class BaseClass final
{
};

class DerivedClass: public BaseClass // compiler error: BaseClass is
                                     // marked as non-inheritable
{
};
```

## <a name="see-also"></a>참고자료

[키워드](../cpp/keywords-cpp.md)<br/>
[override 지정자](../cpp/override-specifier.md)