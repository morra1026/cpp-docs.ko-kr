---
title: locale 클래스
ms.date: 03/19/2019
f1_keywords:
- xlocale/std::locale
- xlocale/std::locale::category
- xlocale/std::locale::combine
- xlocale/std::locale::name
- xlocale/std::locale::classic
- xlocale/std::locale::global
- xlocale/std::locale::operator( )
- xlocale/std::locale::facet
- xlocale/std::locale::id
helpviewer_keywords:
- std::locale [C++]
- std::locale [C++], category
- std::locale [C++], combine
- std::locale [C++], name
- std::locale [C++], classic
- std::locale [C++], global
- std::locale [C++], facet
- std::locale [C++], id
ms.assetid: 7dd6d271-472d-4750-8fb5-ea8f55fbef62
ms.openlocfilehash: a1f5ace58af427645a0ad4eb8706506cc52ab08c
ms.sourcegitcommit: 90817d9d78fbaed8ffacde63f3add334842e596f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "58278517"
---
# <a name="locale-class"></a>locale 클래스

문화별 정보를 특정 지역별 환경을 전체적으로 정의하는 패싯 집합으로 캡슐화하는 로캘 개체에 대해 설명하는 클래스입니다.

## <a name="syntax"></a>구문

```cpp
class locale;
```

## <a name="remarks"></a>설명

패싯은 다음 형식의 공용 개체를 가진 [facet](#facet_class) 클래스에서 파생된 클래스 개체에 대한 포인터입니다.

```cpp
static locale::id id;
```

이러한 패싯의 개방형 집합을 정의할 수 있습니다. 또한 임의 수의 패싯을 지정하는 로캘 개체를 만들 수 있습니다.

이러한 패싯의 미리 정의된 그룹은 일반적으로 `setlocale` 함수에 의해 표준 C 라이브러리에서 관리되는 [로캘 범주](#category)를 나타냅니다.

범주 collate(LC_COLLATE)에 포함되는 패싯:

```cpp
collate<char>
collate<wchar_t>
```

범주 ctype(LC_CTYPE)에 포함되는 패싯:

```cpp
ctype<char>
ctype<wchar_t>
codecvt<char, char, mbstate_t>
codecvt<wchar_t, char, mbstate_t>
codecvt<char16_t, char, mbstate_t>
codecvt<char32_t, char, mbstate_t>
```

범주 monetary(LC_MONETARY)에 포함되는 패싯:

```cpp
moneypunct<char, false>
moneypunct<wchar_t, false>
moneypunct<char, true>
moneypunct<wchar_t, true>
money_get<char, istreambuf_iterator<char>>
money_get<wchar_t, istreambuf_iterator<wchar_t>>
money_put<char, ostreambuf_iterator<char>>
money_put<wchar_t, ostreambuf_iterator<wchar_t>>
```

범주 numeric(LC_NUMERIC)에 포함되는 패싯:

```cpp
num_get<char, istreambuf_iterator<char>>
num_get<wchar_t, istreambuf_iterator<wchar_t>>
num_put<char, ostreambuf_iterator<char>>
num_put<wchar_t, ostreambuf_iterator<wchar_t>>
numpunct<char>
numpunct<wchar_t>
```

범주 time(LC_TIME)에 포함되는 패싯:

```cpp
time_get<char, istreambuf_iterator<char>>
time_get<wchar_t, istreambuf_iterator<wchar_t>>
time_put<char, ostreambuf_iterator<char>>
time_put<wchar_t, ostreambuf_iterator<wchar_t>>
```

범주 messages(LC_MESSAGES)에 포함되는 패싯:

```cpp
messages<char>
messages<wchar_t>
```

(마지막 범주는 Posix에 필요하지만 C 표준은 해당하지 않습니다.)

이러한 미리 정의된 패싯 중 일부는 iostreams 클래스가 숫자 값과 텍스트 시퀀스 사이의 변환을 제어하는 데 사용됩니다.

클래스 로캘 개체는 또한 로캘 이름을 [string](../standard-library/string-typedefs.md#string) 클래스의 개체로 저장합니다. 잘못된 로캘 이름을 사용하여 로캘 패싯 또는 로캘 개체를 만들 경우 [runtime_erro](../standard-library/runtime-error-class.md) 클래스의 개체가 throw됩니다. 로캘 개체를 확인할 수 없고 C-스타일 로캘이 개체로 표현된 로캘에 정확히 해당할 경우 저장된 로캘 이름은 `"*"`입니다. 그러지 않을 경우 로캘 개체 `Loc`에 대해 `setlocale`(LC_ALL `,` `Loc`. [name](#name)`().c_str()`)을 호출하여 표준 C 라이브러리 내에서 일치하는 로캘을 설정할 수 있습니다.

이 구현에서는 정적 멤버 함수도 호출하여

```cpp
static locale empty();
```

패싯이 없는 로캘 개체를 구성할 수 있습니다. 또한 투명 로캘이기도 합니다. 템플릿 함수 [has_facet](../standard-library/locale-functions.md#has_facet) 및 [use_facet](../standard-library/locale-functions.md#use_facet)이 투명 로캘에서 요청된 패싯을 찾을 수 없을 경우 우선 전역 로캘을 참조한 다음, 투명할 경우 클래식 로캘을 참조합니다. 따라서, 다음과 같이 작성할 수 있습니다.

```cpp
cout.imbue(locale::empty());
```

[cout](../standard-library/iostream.md#cout)에 대한 다음 삽입은 전역 로캘의 현재 상태에 따라 조정됩니다. 다음과 같이 작성할 수도 있습니다.

```cpp
locale loc(locale::empty(),
    locale::classic(),
    locale::numeric);

cout.imbue(loc);
```

전역 로캘에서 날짜 및 통화 금액 삽입에 대해 달라진 규칙을 제공하는 경우에도 `cout`에 대한 후속 삽입 숫자 서식 지정 규칙은 C 로캘과 동일하게 유지됩니다.

### <a name="constructors"></a>생성자

|생성자|설명|
|-|-|
|[locale](#locale)|패싯 또는 범주를 다른 로캘의 패싯 또는 범주로 대체한 경우 로캘 또는 로캘의 복사본을 만듭니다.|

### <a name="typedefs"></a>형식 정의

|형식 이름|설명|
|-|-|
|[category](#category)|표준 패싯 범주를 나타내는 비트 마스크 값을 제공하는 정수 형식입니다.|

### <a name="member-functions"></a>멤버 함수

|멤버 함수|설명|
|-|-|
|[combine](#combine)|지정된 로캘의 패싯을 대상 로캘로 삽입합니다.|
|[name](#name)|저장된 로캘 이름을 반환합니다.|

### <a name="static-functions"></a>정적 함수

|||
|-|-|
|[classic](#classic)|정적 멤버 함수는 클래식 C 로캘을 나타내는 로캘 개체를 반환합니다.|
|[global](#global)|프로그램에 대한 기본 로컬을 다시 설정합니다.|

### <a name="operators"></a>연산자

|연산자|설명|
|-|-|
|[operator!=](#op_neq)|두 로캘이 다른지 테스트합니다.|
|[operator( )](#op_call)|두 `basic_string` 개체를 비교합니다.|
|[연산자==](#op_eq_eq)|두 로캘이 같은지 테스트합니다.|

### <a name="classes"></a>클래스

|클래스|설명|
|-|-|
|[facet](#facet_class)|모든 로캘 패싯에 대한 기본 클래스로 사용하는 클래스입니다.|
|[ID](#id_class)|멤버 클래스는 로캘의 패싯을 조회하기 위한 인덱스로 사용되는 고유한 패싯 ID를 제공합니다.|

## <a name="requirements"></a>요구 사항

**헤더:** \<locale>

**네임스페이스:** std

## <a name="category"></a>  locale::category

표준 패싯 범주를 나타내는 비트 마스크 값을 제공하는 정수 형식입니다.

```cpp
typedef int category;
static const int collate = LC_COLLATE;
static const int ctype = LC_CTYPE;
static const int monetary = LC_MONETARY;
static const int numeric = LC_NUMERIC;
static const int time = LC_TIME;
static const int messages = LC_MESSAGES;
static const int all = LC_ALL;
static const int none = 0;
```

### <a name="remarks"></a>설명

형식은의 동의어는 **int** 비트 마스크의 고유 요소 그룹을 나타낼 수 있는 형식 클래스 로캘에 로컬인 입력 하거나 해당 C 로캘 범주 중 하나를 나타내는 데 사용할 수 있습니다. 요소는 다음과 같습니다.

- `collate`에-C 범주 LC_COLLATE에 해당 합니다.

- `ctype`에-C 범주 LC_CTYPE에 해당 합니다.

- `monetary`에-C 범주 LC_MONETARY에 해당 합니다.

- `numeric`에-C 범주 LC_NUMERIC에 해당 합니다.

- `time`에-C 범주 LC_TIME에 해당 합니다.

- `messages`에서 Posix 범주 LC_MESSAGES에 해당 합니다.

또한 두 개의 유용한 값은 다음과 같습니다.

- `none`C 범주 중 어떤 항목에 해당 합니다.

- `all`에 모든 범주 LC_ALL의 C 공용 구조체에 해당 합니다.

임의의 범주 그룹을 사용 하 여 나타낼 수 있습니다 `OR` 에서처럼 이러한 상수를 사용 하 여 `monetary` &#124; `time`합니다.

## <a name="classic"></a>  locale::classic

정적 멤버 함수는 클래식 C 로캘을 나타내는 로캘 개체를 반환합니다.

```cpp
static const locale& classic();
```

### <a name="return-value"></a>반환 값

C 로캘에 대한 참조입니다.

### <a name="remarks"></a>설명

클래식 C 로캘은 국제화되지 않은 프로그램에서 암시적으로 사용되는 표준 C 라이브러리 내의 영어(미국) ASCII 로캘입니다.

### <a name="example"></a>예제

```cpp
// locale_classic.cpp
// compile with: /EHsc
#include <iostream>
#include <string>
#include <locale>

using namespace std;

int main( )
{
   locale loc1( "german" );
   locale loc2 = locale::global( loc1 );
   cout << "The name of the previous locale is: " << loc2.name( )
        << "." << endl;
   cout << "The name of the current locale is: " << loc1.name( )
        << "." << endl;

   if (loc2 == locale::classic( ) )
      cout << "The previous locale was classic." << endl;
   else
      cout << "The previous locale was not classic." << endl;

   if (loc1 == locale::classic( ) )
      cout << "The current locale is classic." << endl;
   else
      cout << "The current locale is not classic." << endl;
}
```

```Output
The name of the previous locale is: C.
The name of the current locale is: German_Germany.1252.
The previous locale was classic.
The current locale is not classic.
```

## <a name="combine"></a>  locale::combine

지정된 로캘의 패싯을 대상 로캘로 삽입합니다.

```cpp
template <class Facet>
locale combine(const locale& Loc) const;
```

### <a name="parameters"></a>매개 변수

*Loc*<br/>
대상 로캘에 삽입할 패싯을 포함하는 로캘입니다.

### <a name="return-value"></a>반환 값

대체 하거나 추가 하는 로캘 개체를 반환 하는 멤버 함수  **\*이** 패싯 `Facet` 나오는 *Loc*합니다.

### <a name="example"></a>예제

```cpp
// locale_combine.cpp
// compile with: /EHsc
#include <locale>
#include <iostream>
#include <tchar.h>
using namespace std;

int main() {
   locale loc ( "German_germany" );
   _TCHAR * s1 = _T("Das ist wei\x00dfzz."); // \x00df is the German sharp-s; it comes before z in the German alphabet
   _TCHAR * s2 = _T("Das ist weizzz.");
   int result1 = use_facet<collate<_TCHAR> > ( loc ).
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );
   cout << isalpha (_T ( '\x00df' ), loc ) << result1 << endl;

   locale loc2 ( "C" );
   int result2 = use_facet<collate<_TCHAR> > ( loc2 ).
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );
   cout << isalpha (_T ( '\x00df' ), loc2 )  << result2 << endl;

   locale loc3 = loc2.combine<collate<_TCHAR> > (loc);
   int result3 = use_facet<collate<_TCHAR> > ( loc3 ).
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );
   cout << isalpha (_T ( '\x00df' ), loc3 ) << result3 << endl;
}
```

## <a name="facet_class"></a>  facet 클래스

모든 로캘 패싯에 대한 기본 클래스로 사용하는 클래스입니다.

```cpp
class facet {
protected:
    explicit facet(size_t _Refs = 0);
   virtual ~facet();
private:
   facet(const facet&)
   // not defined void operator=(const facet&)
     // not defined
};
```

### <a name="remarks"></a>설명

클래스 패싯의 개체를 복사하거나 할당할 수 없습니다. `locale::facet` 클래스에서 파생된 개체는 생성하고 삭제할 수 있지만 기본 클래스 proper의 개체는 생성하고 삭제할 수 없습니다. 일반적으로 **localeloc**( `locale::classic`( ), **new**`_Myfac`);에서처럼 로캘을 생성할 때 패싯에서 파생된 `_Myfac` 개체가 생성됩니다.

이러한 경우 기본 클래스 패싯에 대한 생성자에는 0인`_Refs` 인수가 있어야 합니다. 개체가 더 이상 필요하지 않으면 삭제됩니다. 따라서 개체의 수명을 담당하는 드문 경우에만 0이 아닌 _ *Refs* 인수를 제공합니다.

## <a name="global"></a>  locale::global

프로그램에 대한 기본 로캘을 다시 설정하며, C와 C++ 모두의 전역 로캘에 영향을 줍니다.

```cpp
static locale global(const locale& Loc);
```

### <a name="parameters"></a>매개 변수

*Loc*<br/>
프로그램에서 기본 로캘로 사용할 로캘입니다.

### <a name="return-value"></a>반환 값

기본 로캘이 다시 설정되기 전의 이전 로캘입니다.

### <a name="remarks"></a>설명

프로그램이 시작될 때는 전역 로캘이 클래식 로캘과 같습니다. `global()` 함수는 `setlocale( LC_ALL, loc.name. c_str())`을 호출하여 표준 C 라이브러리에서 일치하는 로캘을 설정합니다.

### <a name="example"></a>예제

```cpp
// locale_global.cpp
// compile by using: /EHsc
#include <locale>
#include <iostream>
#include <tchar.h>
using namespace std;

int main( )
{
   locale loc ( "German_germany" );
   locale loc1;
   cout << "The initial locale is: " << loc1.name( ) << endl;
   locale loc2 = locale::global ( loc );
   locale loc3;
   cout << "The current locale is: " << loc3.name( ) << endl;
   cout << "The previous locale was: " << loc2.name( ) << endl;
}
```

```Output
The initial locale is: C
The current locale is: German_Germany.1252
The previous locale was: C
```

## <a name="id_class"></a>  id 클래스

멤버 클래스는 로캘의 패싯을 조회하기 위한 인덱스로 사용되는 고유한 패싯 ID를 제공합니다.

```cpp
class id 
{
   protected:    id();
   private:      id(const id&)
   void operator=(const id&)  // not defined    
};
```
### <a name="remarks"></a>설명

멤버 클래스는 각 고유 로캘 패싯에 필요한 정적 멤버 개체에 대해 설명합니다. 복사 하거나 클래스의 개체에 할당할 수 없습니다 참고 `id`합니다.

## <a name="locale"></a>  locale::locale

패싯 또는 범주를 다른 로캘의 패싯 또는 범주로 대체한 경우 로캘 또는 로캘의 복사본을 만듭니다.

```cpp
locale();

explicit locale(const char* Locname, category Cat = all);
explicit locale(const string& Locname);
locale( const locale& Loc);
locale(const locale& Loc, const locale& Other, category Cat);
locale(const locale& Loc, const char* Locname, category Cat);

template <class Facet>
locale(const locale& Loc, const Facet* Fac);
```

### <a name="parameters"></a>매개 변수

*Locname*<br/>
로캘 이름입니다.

*Loc*<br/>
새 로캘을 생성할 때 복사되는 로캘입니다.

*기타*<br/>
범주를 선택할 로캘입니다.

*Cat*<br/>
생성된 로캘로 대체될 범주입니다.

*Fac*<br/>
생성된 로캘로 대체될 패싯입니다.

### <a name="remarks"></a>설명

첫 번째 생성자는 전역 로캘과 일치하도록 개체를 초기화합니다. 두 번째 및 세 번째 생성자 초기화 동작이 로캘 이름과 일치 하도록 모든 로캘 범주 *Locname*합니다. 나머지 생성자는 복사 *Loc*를 제외 하 고 있습니다.

`locale(const locale& Loc, const locale& Other, category Cat);`

대체 *다른* 범주에 해당 하는 C는 C에 대 한 패싯을 & *Cat* 0이 아닌 합니다.

`locale(const locale& Loc, const char* Locname, category Cat);`

`locale(const locale& Loc, const string& Locname, category Cat);`

대체 `locale(Locname, _All)` 범주에 해당 하는 C는 C에 대 한 패싯을 & *Cat* 0이 아닌 합니다.

`template<class Facet> locale(const locale& Loc, Facet* Fac);`

대체 (또는 추가) *Loc* 패싯 *Fac*이면 *Fac* 가 null 포인터가 아닌 합니다.

로캘 이름 *Locname* 가 null 포인터 또는 그렇지 않은 경우 잘못 된 경우 함수가 throw [runtime_error](../standard-library/runtime-error-class.md)합니다.

### <a name="example"></a>예제

```cpp
// locale_locale.cpp
// compile with: /EHsc
#include <locale>
#include <iostream>
#include <tchar.h>
using namespace std;

int main( ) {

   // Second constructor
   locale loc ( "German_germany" );
   _TCHAR * s1 = _T("Das ist wei\x00dfzz."); // \x00df is the German sharp-s, it comes before z in the German alphabet
   _TCHAR * s2 = _T("Das ist weizzz.");
   int result1 = use_facet<collate<_TCHAR> > ( loc ).
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );
   cout << isalpha (_T ( '\x00df' ), loc ) << result1 << endl;

   // The first (default) constructor
   locale loc2;
   int result2 = use_facet<collate<_TCHAR> > ( loc2 ).
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );
   cout << isalpha (_T ( '\x00df' ), loc2 )  << result2 << endl;

   // Third constructor
   locale loc3 (loc2,loc, _M_COLLATE );
   int result3 = use_facet<collate<_TCHAR> > ( loc3 ).
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );
   cout << isalpha (_T ( '\x00df' ), loc3 ) << result3 << endl;

   // Fourth constructor
   locale loc4 (loc2, "German_Germany", _M_COLLATE );
   int result4 = use_facet<collate<_TCHAR> > ( loc4 ).
      compare (s1, &s1[_tcslen( s1 )-1 ],  s2, &s2[_tcslen( s2 )-1 ] );
   cout << isalpha (_T ( '\x00df' ), loc4 ) << result4 << endl;
}
```

## <a name="name"></a>  locale::name

저장된 로캘 이름을 반환합니다.

```cpp
string name() const;
```

### <a name="return-value"></a>반환 값

로캘의 이름을 지정하는 문자열입니다.

### <a name="example"></a>예제

```cpp
// locale_name.cpp
// compile with: /EHsc
#include <iostream>
#include <string>
#include <locale>

using namespace std;

int main( )
{
   locale loc1( "german" );
   locale loc2 = locale::global( loc1 );
   cout << "The name of the previous locale is: "
        << loc2.name( ) << "." << endl;
   cout << "The name of the current locale is: "
        << loc1.name( ) << "." << endl;
}
```

```Output
The name of the previous locale is: C.
The name of the current locale is: German_Germany.1252.
```

## <a name="op_neq"></a>  locale::operator!=

두 로캘이 다른지 테스트합니다.

```cpp
bool operator!=(const locale& right) const;
```

### <a name="parameters"></a>매개 변수

*right*<br/>
같지 않음을 테스트할 로캘 중 하나입니다.

### <a name="return-value"></a>반환 값

로캘이 동일한 로캘의 복사본이 아닌 경우 **true**이고 로캘이 동일한 로캘의 복사본인 경우 **false**인 부울 값입니다.

### <a name="remarks"></a>설명

두 로캘은 두 로캘이 동일한 로캘이거나, 한 로캘이 다른 로캘의 복사본이거나, 이름이 동일한 경우 같습니다.

### <a name="example"></a>예제

```cpp
// locale_op_ne.cpp
// compile with: /EHsc
#include <iostream>
#include <string>
#include <locale>

using namespace std;

int main( )
{
   locale loc1( "German_Germany" );
   locale loc2( "German_Germany" );
   locale loc3( "English" );

   if ( loc1 != loc2 )
      cout << "locales loc1 (" << loc1.name( )
      << ") and\n loc2 (" << loc2.name( ) << ") are not equal." << endl;
   else
      cout << "locales loc1 (" << loc1.name( )
      << ") and\n loc2 (" << loc2.name( ) << ") are equal." << endl;

   if ( loc1 != loc3 )
      cout << "locales loc1 (" << loc1.name( )
      << ") and\n loc3 (" << loc3.name( ) << ") are not equal." << endl;
   else
      cout << "locales loc1 (" << loc1.name( )
      << ") and\n loc3 (" << loc3.name( ) << ") are equal." << endl;
}
```

```Output
locales loc1 (German_Germany.1252) and
loc2 (German_Germany.1252) are equal.
locales loc1 (German_Germany.1252) and
loc3 (English_United States.1252) are not equal.
```

## <a name="op_call"></a>  locale::operator()

두 `basic_string` 개체를 비교합니다.

```cpp
template <class CharType, class Traits, class Allocator>
bool operator()(
    const basic_string<CharType, Traits, Allocator>& left,
    const basic_string<CharType, Traits, Allocator>& right) const;
```

### <a name="parameters"></a>매개 변수

*left*<br/>
왼쪽 문자열입니다.

*right*<br/>
오른쪽 문자열입니다.

### <a name="return-value"></a>반환 값

멤버 함수는 다음을 반환합니다.

- 첫 번째 시퀀스가 두 번째 시퀀스보다 작은 것으로 비교되는 경우, -1

- 두 번째 시퀀스가 첫 번째 시퀀스보다 작은 것으로 비교되는 경우, +1

- 시퀀스가 같은 경우, 0

### <a name="remarks"></a>설명

멤버 함수는 다음을 효과적으로 실행합니다.

```cpp
const collate<CharType>& fac = use_fac<collate<CharType>>(*this);

return (fac.compare(left.begin(), left.end(), right.begin(), right.end()) < 0);
```

따라서 로캘 개체를 함수 개체로 사용할 수 있습니다.

### <a name="example"></a>예제

```cpp
// locale_op_compare.cpp
// compile with: /EHsc
#include <iostream>
#include <string>
#include <locale>

int main( )
{
   using namespace std;
   wchar_t *sa = L"ztesting";
   wchar_t *sb = L"\0x00DFtesting";
   basic_string<wchar_t> a( sa );
   basic_string<wchar_t> b( sb );

   locale loc( "German_Germany" );
   cout << loc( a,b ) << endl;

   const collate<wchar_t>& fac = use_facet<collate<wchar_t> >( loc );
   cout << ( fac.compare( sa, sa + a.length( ),
       sb, sb + b.length( ) ) < 0) << endl;
}
```

```Output
0
0
```

## <a name="op_eq_eq"></a>  locale::operator==

두 로캘이 같은지 테스트합니다.

```cpp
bool operator==(const locale& right) const;
```

### <a name="parameters"></a>매개 변수

*right*<br/>
같은지 여부를 테스트할 로캘 중 하나입니다.

### <a name="return-value"></a>반환 값

로캘이 동일한 로캘의 복사본인 경우 **true**이고 로캘이 동일한 로캘의 복사본이 아닌 경우 **false**인 부울 값입니다.

### <a name="remarks"></a>설명

두 로캘은 두 로캘이 동일한 로캘이거나, 한 로캘이 다른 로캘의 복사본이거나, 이름이 동일한 경우 같습니다.

### <a name="example"></a>예제

```cpp
// locale_op_eq.cpp
// compile with: /EHsc
#include <iostream>
#include <string>
#include <locale>

using namespace std;

int main( )
{
   locale loc1( "German_Germany" );
   locale loc2( "German_Germany" );
   locale loc3( "English" );

   if ( loc1 == loc2 )
      cout << "locales loc1 (" << loc1.name( )
      << ")\n and loc2 (" << loc2.name( ) << ") are equal."
      << endl;
   else
      cout << "locales loc1 (" << loc1.name( )
      << ")\n and loc2 (" << loc2.name( ) << ") are not equal."
      << endl;

   if ( loc1 == loc3 )
      cout << "locales loc1 (" << loc1.name( )
      << ")\n and loc3 (" << loc3.name( ) << ") are equal."
      << endl;
   else
      cout << "locales loc1 (" << loc1.name( )
      << ")\n and loc3 (" << loc3.name( ) << ") are not equal."
      << endl;
}
```

```Output
locales loc1 (German_Germany.1252)
and loc2 (German_Germany.1252) are equal.
locales loc1 (German_Germany.1252)
and loc3 (English_United States.1252) are not equal.
```

## <a name="see-also"></a>참고자료

[\<locale>](../standard-library/locale.md)<br/>
[코드 페이지](../c-runtime-library/code-pages.md)<br/>
[로캘 이름, 언어 및 국가/지역 문자열](../c-runtime-library/locale-names-languages-and-country-region-strings.md)<br/>
[C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
