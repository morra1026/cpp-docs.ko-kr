---
title: '방법: 다양한 문자열 형식간 변환'
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- converting string types
- string conversion [C++]
- strings [C++], converting
ms.assetid: e7e4f741-3c82-45f0-b8c0-1e1e343b0e77
ms.openlocfilehash: 8ee8790e960c05827404d932a2305a7de79cbced
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50443357"
---
# <a name="how-to-convert-between-various-string-types"></a>방법: 다양한 문자열 형식간 변환

이 항목에서는 Visual C++에서의 다양한 문자열 형식을 다른 형식으로 변환하는 방법에 대해 설명하며 `char*`, `wchar_t*`, [_bstr_t](../cpp/bstr-t-class.md), [CComBSTR](../atl/reference/ccombstr-class.md), [CString](../atl-mfc-shared/using-cstring.md), [basic_string](../standard-library/basic-string-class.md) 및 <xref:System.String?displayProperty=fullName> 문자열 형식 변환을 다룹니다. 모든 예제에서의 새 형식으로 변환시 문자열에 대한 복사본이 만들어집니다. 새 문자열의 변경사항은 원래 문자열에서 영향을 주지않고, 그 반대의 경우도 마찬가지 입니다.

## <a name="converting-from-char-"></a>char*에서 변환

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예제에서는 `char*` 형식의 문자열을 위에 나열된 다른 문자열 형식으로 변환하는 방법을 보여줍니다. C 스타일 문자열이라고 하는 `char*` 형식의 문자열은 null 문자를 사용하여 문자열의 끝을 나타냅니다. C 스타일 문자열은 대개 문자당 1바이트가 필요하지만 2바이트를 사용할 수도 있습니다. 아래 예에서 `char*` 문자열이 유니코드 문자열에서 변환된 문자열 데이터로, 멀티바이트 문자열이 됩니다. `char*` 문자열은 싱글바이트 및 멀티바이트 문자(`MBCS`) 함수에서 사용할 수 있습니다.

### <a name="code"></a>코드

```cpp
// convert_from_char.cpp
// 컴파일 옵션: /clr /link comsuppw.lib

#include <iostream>
#include <stdlib.h>
#include <string>

#include "atlbase.h"
#include "atlstr.h"
#include "comutil.h"

using namespace std;
using namespace System;

int main()
{
    // C 스타일의 문자열을 화면에 표시한 다음,
    // 이를 여러 종류의 문자열로 변환합니다.
    char *orig = "Hello, World!";
    cout << orig << " (char *)" << endl;

    // newsize는 바이트 수가 아닌 와이드 문자 갯수로,
    // wcstring이라는 wchar_t 타입 문자열의 길이입니다.
    size_t newsize = strlen(orig) + 1;

    // 다음은 원래 문자열의 문자수를 수용할 수 있는
    // 충분한 크기의 버퍼를 만듭니다.
    // 문자열에 더 많은 문자를 추가하려면 newsize 값을
    // 늘려 버퍼의 크기를 늘립니다.
    wchar_t * wcstring = new wchar_t[newsize];

    // char* 문자열을 wchar_t* 타입으로 변환합니다.
    size_t convertedChars = 0;
    mbstowcs_s(&convertedChars, wcstring, newsize, orig, _TRUNCATE);
    // 결과를 표시하고 문자열의 타입을 표시합니다.
    wcout << wcstring << _T(" (wchar_t *)") << endl;

    // C 스타일 문자열을 _bstr_t 문자열로 변환합니다.
    _bstr_t bstrt(orig);
    // 문자열 타입을 새 문자열에 추가한다음
    // 결과를 화면에 표시합니다.
    bstrt += " (_bstr_t)";
    cout << bstrt << endl;

    // C 스타일 문자열을 CComBSTR 문자열로 변환합니다.
    CComBSTR ccombstr(orig);
    if (ccombstr.Append(_T(" (CComBSTR)")) == S_OK)
    {
        CW2A printstr(ccombstr);
        cout << printstr << endl;
    }

    // C 스타일 문자열을 CStringA로 변환하여 표시합니다.
    CStringA cstringa(orig);
    cstringa += " (CStringA)";
    cout << cstringa << endl;

    // C 스타일 문자열을 CStringW로 변환하여 표시합니다.
    CStringW cstring(orig);
    cstring += " (CStringW)";
    // CStringW를 화면에 정확히 표시하기 위해 wcout을
    // 사용하고, LPCWSTR 형식으로 형변환 합니다.
    wcout << (LPCTSTR)cstring << endl;

    // C 스타일 문자열을 basic_string으로 변환하여 표시합니다.
    string basicstring(orig);
    basicstring += " (basic_string)";
    cout << basicstring << endl;

    // C 스타일 문자열을 System::String으로 변환하여 표시합니다.
    String ^systemstring = gcnew String(orig);
    systemstring += " (System::String)";
    Console::WriteLine("{0}", systemstring);
    delete systemstring;
}
```

```Output
Hello, World! (char *)
Hello, World! (wchar_t *)
Hello, World! (_bstr_t)
Hello, World! (CComBSTR)
Hello, World! (CStringA)
Hello, World! (CStringW)
Hello, World! (basic_string)
Hello, World! (System::String)
```

## <a name="converting-from-wchart-"></a>wchar_t*에서 변환

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예제에서는 `char*` 형식의 문자열을 위에 나열된 다른 문자열 형식으로 변환하는 방법을 보여줍니다. C 스타일 문자열이라고 하는 `char*` 형식의 문자열은 null 문자를 사용하여 문자열의 끝을 나타냅니다. C 스타일 문자열은 대개 문자당 1바이트가 필요하지만 2바이트를 사용할 수도 있습니다. 아래 예에서 `char*` 문자열이 유니코드 문자열에서 변환된 문자열 데이터로, 멀티바이트 문자열이 됩니다. `char*` 문자열은 싱글바이트 및 멀티바이트 문자(`MBCS`) 함수에서 사용할 수 있습니다.

### <a name="code"></a>코드

```cpp
// convert_from_wchar_t.cpp
// 컴파일 옵션: /clr /link comsuppw.lib

#include <iostream>
#include <stdlib.h>
#include <string>

#include "atlbase.h"
#include "atlstr.h"
#include "comutil.h"

using namespace std;
using namespace System;

int main()
{
    // 와이드 문자 기반의 문자열을 화면에 표시한 다음,
    // 이를 여러 종류의 문자열로 변환합니다.
    wchar_t *orig = _T("Hello, World!");
    wcout << orig << _T(" (wchar_t *)") << endl;

    // wchar_t 기반 문자열을 char* 문자열로 변환합니다.
    // 원래 문자열의 길이를 저장하고 null문자를 위해
    // origsize에 1을 더 추가합니다.
    size_t origsize = wcslen(orig) + 1;
    size_t convertedChars = 0;

    // 멀티바이트 문자열을 사용하여 결과를 표시하기 전에 
    // 문자열 형식을 새 문자열에 추가합니다.
    char strConcat[] = " (char *)";
    size_t strConcatsize = (strlen( strConcat ) + 1)*2;

    // 와이드 문자 null을 포함한 입력된 문자열의
    // 모든 와이드 문자에 대한 멀티바이트의 받는 문자열에
    // 2바이트를 할당합니다. 멀티바이트 문자는 1바이트나
    // 2바이트가 될 수 있으므로, 각 문자에 대해 2바이트를
    // 할당해야합니다. 새 문자열을 위해 여유 공간을 확보하는
    // 것은 문제가 되지 않지만, 공간이 충분치 않다는건
    // 잠재적인 보안문제 입니다.
    const size_t newsize = origsize*2;
    // 새로운 문자열에는 기존 문자열이 변환된 복사본과
    // 거기에 문자열 형식이 추가됩니다.
    char *nstring = new char[newsize+strConcatsize];

    // 변환되는 문자열을 nstring에 복사합니다
    wcstombs_s(&convertedChars, nstring, newsize, orig, _TRUNCATE);
    // 문자열 형식을 새 문자열에 추가합니다.
    _mbscat_s((unsigned char*)nstring, newsize+strConcatsize, (unsigned char*)strConcat);
    // 결과물를 표시합니다.
    cout << nstring << endl;

    // wchar_t 기반의 문자열을 _bstr_t 기반의 문자열로 변환하여 표시합니다.
    _bstr_t bstrt(orig);
    bstrt += " (_bstr_t)";
    cout << bstrt << endl;

    // BSTR 문자열을 만들기 위해 ATL의 CComBSTR 래퍼클래스를 이용하여
    // wchar_t 기반의 문자열을 BSTR 와이드 문자열로 변환합니다.
    // 변환 후 결과물을 표시합니다.
    CComBSTR ccombstr(orig);
    if (ccombstr.Append(_T(" (CComBSTR)")) == S_OK)
    {
        // CW2A를 이용해 ccombstr을 멀티바이트 기반인 printstr로
        // 변환 후 화면에 표시합니다.
        CW2A printstr(ccombstr);
        cout << printstr << endl;
        // 다음과 같은 코드를 통해 와이드 문자 기반 문자열을 
        // 쉽게 표시할 수 있습니다.
        wcout << (LPCWSTR) ccombstr << endl;
    }

    // 와이드 문자 형식인 wchar_t 기반인 문자열을 멀티바이트 형식인 CStringA로
    // 변환하고 스트링 형식을 추가합니다. 그리고 화면에 표시 합니다.
    CStringA cstringa(orig);
    cstringa += " (CStringA)";
    cout << cstringa << endl;

    // 와이드 문자 형식인 wchar_t 기반 문자열을 같은 문자 형식 기반인 CStringW로
    // 대입하고 스트링 형식을 추가합니다.
    CStringW cstring(orig);
    cstring += " (CStringW)";
    // CStringW 문자열을 바르게 출력하기 위해 wcout과 (LPCWSTR) 형식으로
    // 문자열을 형변환 합니다.
    wcout << (LPCWSTR)cstring << endl;

    // 와이드 문자 형식은 wchar_t 기반 문자열을 basic_string으로 변환하고
    // 스트링 형식을 추가한 후 결과를 화면에 표시 합니다.
    wstring basicstring(orig);
    basicstring += _T(" (basic_string)");
    wcout << basicstring << endl;

    // 와이드 문자 wchar_t 기반 문자열을 System::String 문자열로 변환하고
    // 문자열의 타입을 추가한 후 결과물을 화면에 표시합니다.
    String ^systemstring = gcnew String(orig);
    systemstring += " (System::String)";
    Console::WriteLine("{0}", systemstring);
    delete systemstring;
}
```

```Output
Hello, World! (wchar_t *)
Hello, World! (char *)
Hello, World! (_bstr_t)
Hello, World! (CComBSTR)
Hello, World! (CStringA)
Hello, World! (CStringW)
Hello, World! (basic_string)
Hello, World! (System::String)
```

## <a name="converting-from-bstrt"></a>_bstr_t에서 변환

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예제에서는 `_bstr_t` 형식의 문자열을 처음에 나열된 다른 문자열 유형으로 변환하는 방법을 보여줍니다. `_bstr_t` 개체는 와이드 문자기반 `BSTR` 문자열을 캡슐화 합니다. `BSTR` 문자열은 길이 값을 가지고 있고, 문자열의 끝을 표현하는데 null문자를 사용하지는 않습니다. 따라서 변환될 문자열 형식은 문자열 끝 표현을 위한 null 문자 추가가 필요할 수 있습니다.

### <a name="code"></a>코드

```cpp
// convert_from_bstr_t.cpp
// 컴파일 옵션: /clr /link comsuppw.lib

#include <iostream>
#include <stdlib.h>
#include <string>

#include "atlbase.h"
#include "atlstr.h"
#include "comutil.h"

using namespace std;
using namespace System;

int main()
{
    // _bstr_t 문자열 개체를 만들고 화면에 
    // 생성한 문자열과 개체 타입을 표시합니다.
    _bstr_t orig("Hello, World!");
    wcout << orig << " (_bstr_t)" << endl;

    // 와이드 문자 기반의 _bstr_t 문자열을 C 스타일의 문자열로
    // 변환합니다. 안전한 변환을 위해 char* 문자열을 구성하는 문자마다
    // 2바이트를 할당합니다. 여기엔 문자열 종료를 위한 null문자도
    // 포함됩니다.
    const size_t newsize = (orig.length()+1)*2;
    char *nstring = new char[newsize];

    // _bstr_t의 (char*) 형식으로 형변환하는 연산자를 이용해
    // nstring에 _bstr_t 객체에서 null 문자로 끝나는 문자열을
    // 복사하고 형식을 추가한 후 화면에 표시 합니다.
    strcpy_s(nstring, newsize, (char *)orig);
    strcat_s(nstring, newsize, " (char *)");
    cout << nstring << endl;

    // 결과에 추가할 문자열 형식을 준비합니다.
    wchar_t strConcat[] = _T(" (wchar_t *)");
    size_t strConcatLen = wcslen(strConcat) + 1;

    // _bstr_t에서 wchar_t* 형식의 문자열로 변환합니다.
    const size_t widesize = orig.length()+ strConcatLen;
    wchar_t *wcstring = new wchar_t[newsize];
    wcscpy_s(wcstring, widesize, (wchar_t *)orig);
    wcscat_s(wcstring, widesize, strConcat);
    wcout << wcstring << endl;

    // _bstr_t에서 CComBSTR 문자열로 변환합니다.
    CComBSTR ccombstr((char *)orig);
    if (ccombstr.Append(_T(" (CComBSTR)")) == S_OK)
    {
        CW2A printstr(ccombstr);
        cout << printstr << endl;
    }

    // _bstr_t에서 CStringA 문자열로 변환합니다.
    CStringA cstringa(orig.GetBSTR());
    cstringa += " (CStringA)";
    cout << cstringa << endl;

    // _bstr_t에서 CStringW 문자열로 변환합니다.
    CStringW cstring(orig.GetBSTR());
    cstring += " (CStringW)";
    // 올바르게 출력하기 위해 wcout을 사용하고
    // (LPCWSTR)로 형변환 합니다.
    wcout << (LPCWSTR)cstring << endl;

    // _bstr_t에서 basic_string으로 변환합니다.
    string basicstring((char *)orig);
    basicstring += " (basic_string)";
    cout << basicstring << endl;

    // _bstr_t에서 System::String으로 변환합니다.
    String ^systemstring = gcnew String((char *)orig);
    systemstring += " (System::String)";
    Console::WriteLine("{0}", systemstring);
    delete systemstring;
}
```

```Output
Hello, World! (_bstr_t)
Hello, World! (char *)
Hello, World! (wchar_t *)
Hello, World! (CComBSTR)
Hello, World! (CStringA)
Hello, World! (CStringW)
Hello, World! (basic_string)
Hello, World! (System::String)
```

## <a name="converting-from-ccombstr"></a>CComBSTR에서 변환

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예제에서는 `CComBSTR` 형식의 문자열을 처음에 나열된 다른 문자열 유형으로 변환하는 방법을 보여줍니다. `CComBSTR`은 `_bstr_t`와 같이 와이드 문자기반 `BSTR` 문자열을 캡슐화 합니다. `BSTR` 문자열은 길이 값을 가지고 있고, 문자열의 끝을 표현하는데 null문자를 사용하지는 않습니다. 따라서 변환될 문자열 형식은 문자열 끝 표현을 위한 null 문자 추가가 필요할 수 있습니다.

### <a name="code"></a>코드

```cpp
// convert_from_ccombstr.cpp
// 컴파일 옵션: /clr /link comsuppw.lib

#include <iostream>
#include <stdlib.h>
#include <string>

#include "atlbase.h"
#include "atlstr.h"
#include "comutil.h"
#include "vcclr.h"

using namespace std;
using namespace System;
using namespace System::Runtime::InteropServices;

int main()
{
    // CComBSTR 개체에 BSTR 문자열을 만들어 초기화 합니다.
    CComBSTR orig("Hello, World!");
    // BSTR을 멀티바이트 문자열로 변환하고, 결과를 표시한 후
    // 문자열 형식을 표시합니다.
    CW2A printstr(orig);
    cout << printstr << " (CComBSTR)" << endl;

    // 와이드 문자 기반 CComBSTR 문자열을 일반적인
    // 멀티바이트 char* 문자열로 변환합니다.
    // 가장 많은 공간을 차지할 경우를 가정하여 새로운 문자열을 위한
    // 충분한 공간을 확보합니다. 여기에는 문자열 끝을 의미하는
    // null 문자의 공간도 포함됩니다.
    const size_t newsize = (orig.Length()+1)*2;
    char *nstring = new char[newsize];

    // 문자열 변환 객체를 만들고 새 char* 문자열에 복하한 다음
    // 결과를 화면에 표시합니다.
    CW2A tmpstr1(orig);
    strcpy_s(nstring, newsize, tmpstr1);
    cout << nstring << " (char *)" << endl;

    // 결과에 추가할 문자열 형식 문자열을 준비합니다.
    wchar_t strConcat[] = _T(" (wchar_t *)");
    size_t strConcatLen = wcslen(strConcat) + 1;

    // 와이드 문자 기반 CComBSTR 문자열을 wchar_t*로 변환합니다.
    // 변환된 문자열의 길이와 추가된 형식 문자열 길이를 정한다음
    // 화면에 표시할 wchar_t 문자 기반 문자열을 준비합니다.
    const size_t widesize = orig.Length()+ strConcatLen;
    wchar_t *wcstring = new wchar_t[widesize];
    wcscpy_s(wcstring, widesize, orig);
    wcscat_s(wcstring, widesize, strConcat);

    // 결과를 표시합니다. CStringW와는 달리 wchar_t는 wcout을 이용할 때
    // (LPCWSTR)으로의 형변환이 필요하지 않습니다.
    wcout << wcstring << endl;

    // 와이드 문자 기반 CComBSTR을 같은 와이드 문자 기반인 _bstr_t로
    // 변환하고, 문자열 형식을 추가한 다음 화면에 표시합니다.
    _bstr_t bstrt(orig);
    bstrt += " (_bstr_t)";
    cout << bstrt << endl;

    // 와이드 문자기반 CComBSTR을 멀티바이트의 CStringA로 변환하고
    // 문자열 형식을 추가한 다음 결과물을 화면에 표시합니다.
    CStringA cstringa(orig);
    cstringa += " (CStringA)";
    cout << cstringa << endl;

    // 와이드 문자 기반의 CComBSTR을 와이드 문자 기반인 CStringW로
    // 변환합니다.
    CStringW cstring(orig);
    cstring += " (CStringW)";
    // cstring을 올바르게 표시하기 위해 wcout과 함께 (LPCWSTR)로
    // 형변환 합니다.
    wcout << (LPCWSTR)cstring << endl;

    // 와이드 문자 기반 CComBSTR을 와이드 문자 기반의
    // basic_string으로 변환합니다.
    wstring basicstring(orig);
    basicstring += _T(" (basic_string)");
    wcout << basicstring << endl;

    // 와이드 문자 기반의 CComBSTR을 System::String으로
    // 변환합니다.
    String ^systemstring = gcnew String(orig);
    systemstring += " (System::String)";
    Console::WriteLine("{0}", systemstring);
    delete systemstring;
}
```

```Output
Hello, World! (CComBSTR)
Hello, World! (char *)
Hello, World! (wchar_t *)
Hello, World! (_bstr_t)
Hello, World! (CStringA)
Hello, World! (CStringW)
Hello, World! (basic_string)
Hello, World! (System::String)
```

## <a name="converting-from-cstring"></a>CString에서 변환

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예제에서는 `CString` 형식의 문자열을 처음에 나열된 다른 문자열 형식으로 변환하는 방법을 보여줍니다. `CString`은 `_UNICODE` 심볼의 정의 여부에 따라 형식이 달라지는 TCHAR 데이터 형식 기반의 문자열 입니다. `TCHAR`는 `_UNICODE`가 정의되어 있지 않다면 `char`로 정의되어 `CString`은 멀티바이트 문자열이 포함됩니다. `_UNICODE`가 정의되었다면 `TCHAR`는 `wchar_t`로 정의되며 `CString`은 와이드 문자열 기반이 됩니다.

`CStringA`는 멀티바이트 기반 전용 문자열이며 `CStringW`는 와이드 기반 전용 문자열입니다. `CStringA`와 `CStringW`는 `_UNICODE`의 정의여부에 따라 컴파일시 기반 형식이 달라지지 않습니다. 이 예제에서의 `CStringA`와 `CStringW`의 구분은, 버퍼 크기 할당이나 출력을 올바르게 처리하기 위한 사소한 차이점을 명확하게 전달하기 위하여 사용됩니다.

### <a name="code"></a>코드

```cpp
// convert_from_cstring.cpp
// 컴파일 옵션: /clr /link comsuppw.lib

#include <iostream>
#include <stdlib.h>
#include <string>

#include "atlbase.h"
#include "atlstr.h"
#include "comutil.h"

using namespace std;
using namespace System;

int main()
{
    // 멀티바이트 CStringA 문자열을 설정합니다.
    CStringA origa("Hello, World!");
    cout << origa << " (CStringA)" << endl;

    // 와이드 문자 기반의 CStringW 문자열을 설정합니다.
    CStringW origw("Hello, World!");
    wcout << (LPCWSTR)origw << _T(" (CStringW)") << endl;

    // CStringA 문자열을 char* 문자열로 변환하고
    // 화면에 표시합니다.
    const size_t newsizea = (origa.GetLength() + 1);
    char *nstringa = new char[newsizea];
    strcpy_s(nstringa, newsizea, origa);
    cout << nstringa << " (char *)" << endl;

    // 와이드 문자 기반 CStringW 문자열을 char* 문자열로
    // 변환합니다. 안전한 변환을 위해 char* 문자열을 구성하는 문자마다
    // 2바이트를 할당합니다. 여기엔 문자열 종료를 위한 null문자도
    // 포함됩니다. 
    const size_t newsizew = (origw.GetLength() + 1)*2;
    char *nstringw = new char[newsizew];
    size_t convertedCharsw = 0;
    wcstombs_s(&convertedCharsw, nstringw, newsizew, origw, _TRUNCATE );
    cout << nstringw << " (char *)" << endl;
    
    // CStringA를 wchar_t* 문자열로 변환합니다.
    size_t convertedCharsa = 0;
    wchar_t *wcstring = new wchar_t[newsizea];
    mbstowcs_s(&convertedCharsa, wcstring, newsizea, origa, _TRUNCATE);
    wcout << wcstring << _T(" (wchar_t *)") << endl;

    // 와이드 문자기반 CStringW 문자열을 같은 와이드 문자 기반
    // wchar_t* 문자열로 변환합니다.
    wchar_t *n2stringw = new wchar_t[newsizew];
    wcscpy_s( n2stringw, newsizew, origw );
    wcout << n2stringw << _T(" (wchar_t *)") << endl;

    // 멀티바이트 CStringA를 와이드 문자 기반 _bstr_t 문자열로
    // 변환합니다.
    _bstr_t bstrt(origa);
    bstrt += _T(" (_bstr_t)");
    wcout << bstrt << endl;

    // 와이드 문자 기반 CStringW 문자열을 같은 와이드 문가 기반
    // _bstr_t 문자열로 변환합니다.
    bstr_t bstrtw(origw);
    bstrtw += " (_bstr_t)";
    wcout << bstrtw << endl;

    // 멀티바이트 문자 기반 CStringA 문자열을 와이드 문자 기반
    // CComBSTR 문자열로 변환합니다.
    CComBSTR ccombstr(origa);
    if (ccombstr.Append(_T(" (CComBSTR)")) == S_OK)
    {
        // 와이드 문자 기반 문자열을 출력을 위해 멀티바이트로
        // 변환합니다.
        CW2A printstr(ccombstr);
        cout << printstr << endl;
    }
    
    // 와이드 문자 기반의 CStringW 문자열을 같은 와이드 문자 기반
    // CComBSTR 문자열로 변환합니다.
    CComBSTR ccombstrw(origw);
    
    // 문자열 형식을 붙이고, 화면에 표시합니다.
    if (ccombstrw.Append(_T(" (CComBSTR)")) == S_OK)
    {
        CW2A printstrw(ccombstrw);
        wcout << printstrw << endl;
    }
    
    // 멀티바이트 문자 기반 CStringA를 멀티바이트 형식 기반의
    // basic_string 문자열로 변환합니다.
    string basicstring(origa);
    basicstring += " (basic_string)";
    cout << basicstring << endl;
    
    // 와이드 문자 기반의 CStringW를 와이드 문자 기반의
    // basic_string 문자열로 변환합니다.
    wstring basicstringw(origw);
    basicstringw += _T(" (basic_string)");
    wcout << basicstringw << endl;
    
    // 멀티바이트 문자 기반 CStringA를 System::String으로
    // 변환합니다.
    String ^systemstring = gcnew String(origa);
    systemstring += " (System::String)";
    Console::WriteLine("{0}", systemstring);
    delete systemstring;
    
    // 와이드 문자 기반 CStringW를 System::String으로
    // 변환합니다.
    String ^systemstringw = gcnew String(origw);
    systemstringw += " (System::String)";
    Console::WriteLine("{0}", systemstringw);
    delete systemstringw;
}
```

```Output
Hello, World! (CStringA)
Hello, World! (CStringW)
Hello, World! (char *)
Hello, World! (char *)
Hello, World! (wchar_t *)
Hello, World! (wchar_t *)
Hello, World! (_bstr_t)
Hello, World! (_bstr_t)
Hello, World! (CComBSTR)
Hello, World! (CComBSTR)
Hello, World! (basic_string)
Hello, World! (System::String)
```

## <a name="converting-from-basicstring"></a>basic_string에서 변환

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예제에서는 `basic_string`을 처음에 나열된 다른 문자열 형식으로 변환하는 방법을 보여줍니다.

### <a name="code"></a>코드

```cpp
// convert_from_basic_string.cpp
// 컴파일 옵션: /clr /link comsuppw.lib

#include <iostream>
#include <stdlib.h>
#include <string>

#include "atlbase.h"
#include "atlstr.h"
#include "comutil.h"

using namespace std;
using namespace System;

int main()
{
    // basic_string 문자열을 설정합니다.
    string orig("Hello, World!");
    cout << orig << " (basic_string)" << endl;

    // 와이드 문자 기반 basic_string 문자열을 멀티바이트 char* 문자열로
    // 변환합니다. 안전한 변환을 위해 문자열을 구성하는 문자마다
    // 2바이트를 할당합니다. 여기엔 문자열 종료를 위한 null문자도
    // 포함됩니다. 
    const size_t newsize = (strlen(orig.c_str()) + 1)*2;
    char *nstring = new char[newsize];
    strcpy_s(nstring, newsize, orig.c_str());
    cout << nstring << " (char *)" << endl;

    // basic_string 문자열을 와이드 문자 wchar_t* 문자열로
    // 변환합니다. 이를 위해 먼저 char*로 변환합니다.
    const size_t newsizew = strlen(orig.c_str()) + 1;
    size_t convertedChars = 0;
    wchar_t *wcstring = new wchar_t[newsizew];
    mbstowcs_s(&convertedChars, wcstring, newsizew, orig.c_str(), _TRUNCATE);
    wcout << wcstring << _T(" (wchar_t *)") << endl;

    // basic_string 문자열을 와이드 문자 기반 _bstr_t 문자열로
    // 변환합니다.
    _bstr_t bstrt(orig.c_str());
    bstrt += _T(" (_bstr_t)");
    wcout << bstrt << endl;

    // basic_string 문자열을 와이드 문자 기반 CComBSTR 문자열로
    // 변환합니다.
    CComBSTR ccombstr(orig.c_str());
    if (ccombstr.Append(_T(" (CComBSTR)")) == S_OK)
    {
        // 멀티바이트 기반의 CComBSTR 문자열을 만들고
        // 결과물을 화면에 표시합니다.
        CW2A printstr(ccombstr);
        cout << printstr << endl;
    }

    // basic_string 문자열을 멀티바이트 CStringA 문자열로
    // 변환합니다.
    CStringA cstring(orig.c_str());
    cstring += " (CStringA)";
    cout << cstring << endl;

    // basic_string 문자열을 와이드 문자 기반 CStringW 문자열로
    // 변환합니다.
    CStringW cstringw(orig.c_str());
    cstringw += _T(" (CStringW)");
    wcout << (LPCWSTR)cstringw << endl;

    // basic_string 문자열을 System::String 문자열로
    // 변환합니다.
    String ^systemstring = gcnew String(orig.c_str());
    systemstring += " (System::String)";
    Console::WriteLine("{0}", systemstring);
    delete systemstring;
}
```

```Output
Hello, World! (basic_string)
Hello, World! (char *)
Hello, World! (wchar_t *)
Hello, World! (_bstr_t)
Hello, World! (CComBSTR)
Hello, World! (CStringA)
Hello, World! (CStringW)
Hello, World! (System::String)
```

## <a name="converting-from-systemstring"></a>System::String에서 변환

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예제에서는 유니코드인 와이드 문자 기반 [System::String](assetId:///System::String?qualifyHint=True&autoUpgrade=True)을 처음에 나열된 다른 문자열 유형으로 변환하는 방법을 보여줍니다.

### <a name="code"></a>코드

```cpp
// convert_from_system_string.cpp
// 컴파일 옵션: /clr /link comsuppw.lib

#include <iostream>
#include <stdlib.h>
#include <string>

#include "atlbase.h"
#include "atlstr.h"
#include "comutil.h"
#include "vcclr.h"

using namespace std;
using namespace System;
using namespace System::Runtime::InteropServices;

int main()
{
    // System::String을 설정하고 결과물을 화면에 표시합니다.
    String ^orig = gcnew String("Hello, World!");
    Console::WriteLine("{0} (System::String)", orig);

    // System::String의 포인터를 가져와 가비지 컬렉터(GC)가
    // 네이티브 함수를 호출하는 동안 개체를 이동시키지 못하도록
    // 먼저 메모리를 잠급니다.
    pin_ptr<const wchar_t> wch = PtrToStringChars(orig);

    // System::String 문자열의 멀티바이트 char* 문자열
    // 복사본을 만듭니다. 문장의 종료를 표현하는 null문자를 포함,
    // 모든 와이드 입력 문자에 대하여 출력되는 멀티바이트 문자열은
    // 글자마다 2바이트를 할당합니다.
    size_t origsize = wcslen(wch) + 1;
    const size_t newsize = origsize*2;
    size_t convertedChars = 0;
    char *nstring = new char[newsize];
    wcstombs_s(&convertedChars, nstring, newsize, wch, _TRUNCATE);
    cout << nstring << " (char *)" << endl;

    // 와이드 문자 기반 System::String을 같은 와이드 문자 기반
    // wchar_t* 문자열로 변환합니다.
    const size_t newsizew = origsize;
    wchar_t *wcstring = new wchar_t[newsizew];
    wcscpy_s(wcstring, newsizew, wch);
    wcout << wcstring << _T(" (wchar_t *)") << endl;

    // 와이드 문자 기반 System::String을 같은 와이드 문자 기반
    // _bstr_t 문자열로 변환합니다.
    _bstr_t bstrt(wch);
    bstrt += " (_bstr_t)";
    cout << bstrt << endl;

    // 와이드 문자 기반 System::String을 같은 와이드 문자 기반
    // CComBSTR 문자열로 변환합니다.
    CComBSTR ccombstr(wch);
    if (ccombstr.Append(_T(" (CComBSTR)")) == S_OK)
    {
        // 멀티바이트 기반의 CComBSTR 문자열 복사본을 만들어
        // 화면에 표시합니다.
        CW2A printstr(ccombstr);
        cout << printstr << endl;
    }

    // 와이드 문자 기반의 System::String을
    // 멀티바이트 CStringA 문자열로 변환합니다.
    CStringA cstring(wch);
    cstring += " (CStringA)";
    cout << cstring << endl;

    // 와이드 문자 기반의 System::String을
    // 같은 와이드 문자 CStringW 문자열로 변환합니다.
    CStringW cstringw(wch);
    cstringw += " (CStringW)";
    wcout << (LPCWSTR)cstringw << endl;

    // 와이드 문자 기반의 System::String을
    // 같은 와이드 문자 기반의 basic_string으로 변환합니다.
    wstring basicstring(wch);
    basicstring += _T(" (basic_string)");
    wcout << basicstring << endl;

    delete orig;
}
```

```Output
Hello, World! (System::String)
Hello, World! (char *)
Hello, World! (wchar_t *)
Hello, World! (_bstr_t)
Hello, World! (CComBSTR)
Hello, World! (CStringA)
Hello, World! (CStringW)
Hello, World! (basic_string)
```

## <a name="see-also"></a>참고 항목

[ATL 및 MFC 문자열 변환 매크로](../atl/reference/string-conversion-macros.md)<br/>
[C 스타일 문자열 관련 CString 작업](../atl-mfc-shared/cstring-operations-relating-to-c-style-strings.md)<br/>
[방법: 표준 문자열을 System::String으로 변환](../dotnet/how-to-convert-standard-string-to-system-string.md)<br/>
[방법: System::String을 표준 문자열로 변환](../dotnet/how-to-convert-system-string-to-standard-string.md)<br/>
[방법: System::String을 wchar_t* 또는 char*로](../dotnet/how-to-convert-system-string-to-wchar-t-star-or-char-star.md)<br/>
[CComBSTR을 사용한 프로그래밍](../atl/programming-with-ccombstr-atl.md)<br/>
[mbstowcs_s, _mbstowcs_s_l](../c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l.md)<br/>
[wcstombs_s, _wcstombs_s_l](../c-runtime-library/reference/wcstombs-s-wcstombs-s-l.md)<br/>
[strcpy_s, wcscpy_s, _mbscpy_s](../c-runtime-library/reference/strcpy-s-wcscpy-s-mbscpy-s.md)<br/>
[strcat_s, wcscat_s, _mbscat_s](../c-runtime-library/reference/strcat-s-wcscat-s-mbscat-s.md)<br/>
[pin_ptr(C++/CLI)](../windows/pin-ptr-cpp-cli.md)
