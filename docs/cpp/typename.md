---
title: typename
ms.date: 11/04/2016
f1_keywords:
- typename_cpp
helpviewer_keywords:
- typename template specifier
ms.assetid: 52e1d901-220d-4f0d-ab43-dae7e05fb491
ms.openlocfilehash: 7dbe4381465036bdd102b3be753a18451886a3d8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50665857"
---
# <a name="typename"></a>typename

템플릿 정의에서 알 수 없는 식별자가 형식이라는 힌트를 컴파일러에 알려줍니다. 템플릿 매개변수 목록에서 형식 매개변수를 지정하는데 사용됩니다.

## <a name="syntax"></a>구문

```
typename identifier;
```

## <a name="remarks"></a>설명

This keyword must be used if a name in a template definition is a qualified name that is dependent on a template argument; it is optional if the qualified name is not dependent. For more information, see Templates and Name Resolution.
템플릿 정의에서의 이름이 템플릿 인수에 속하는 한정된 이름(Qualified name)인 경우 이 키워드를 사용합니다.  한정된 이름이 종속성은 선택사항 입니다. 자세한 내용은 [템플릿 및 이름 확인](../cpp/templates-and-name-resolution.md)을 참조합니다.

**typename**은 템플릿 정의나 선언의 어디에서나 사용할 수 있습니다. 템플릿 기반 클래스(Base class)에 대한 템플릿 인수로 사용되지 않는 한 기반 클래스 목록에는 사용할 수 없습니다.

```cpp
template <class T>
class C1 : typename T::InnerType // 오류 - typename은 허용되지 않습니다.
{};
template <class T>
class C2 : A<typename T::InnerType>  // typename OK.
{};
```

템플릿 매개변수 목록에 **class** 대신 **typename** 키워드를 대신 사용할 수도 있습니다. 예를 들어 다음은 의미상 동일합니다.

```cpp
template<class T1, class T2>...
template<typename T1, typename T2>...
```

## <a name="example"></a>예제

```cpp
// typename.cpp
template<class T> class X
{
   typename T::Y m_y;   // Y를 형식으로 취급합니다.
};

int main()
{
}
```

## <a name="see-also"></a>참고자료

[템플릿](../cpp/templates-cpp.md)<br/>
[키워드](../cpp/keywords-cpp.md)
