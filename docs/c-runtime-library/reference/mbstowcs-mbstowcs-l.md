---
title: mbstowcs, _mbstowcs_l
ms.date: 11/04/2016
apiname:
- mbstowcs
- _mbstowcs_l
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-multibyte-l1-1-0.dll
- api-ms-win-crt-convert-l1-1-0.dll
- ntoskrnl.exe
apitype: DLLExport
f1_keywords:
- mbstowcs
helpviewer_keywords:
- _mbstowcs_l function
- mbstowcs_l function
- mbstowcs function
ms.assetid: 96696b27-e068-4eeb-8006-3f7a0546ae6d
ms.openlocfilehash: b9178f64dd698ff517ea5b376ed19e97981c511d
ms.sourcegitcommit: e06648107065f3dea35f40c1ae5999391087b80b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57210681"
---
# <a name="mbstowcs-mbstowcsl"></a>mbstowcs, _mbstowcs_l

멀티바이트 문자 시퀀스를 해당 와이드 문자 시퀀스로 변환합니다. 이러한 함수의 더 안전한 버전을 사용할 수 있습니다. [mbstowcs_s, _mbstowcs_s_l](mbstowcs-s-mbstowcs-s-l.md)을 참조하세요.

## <a name="syntax"></a>구문

```C
size_t mbstowcs(
   wchar_t *wcstr,
   const char *mbstr,
   size_t count
);
size_t _mbstowcs_l(
   wchar_t *wcstr,
   const char *mbstr,
   size_t count,
   _locale_t locale
);
template <size_t size>
size_t mbstowcs(
   wchar_t (&wcstr)[size],
   const char *mbstr,
   size_t count
); // C++ only
template <size_t size>
size_t _mbstowcs_l(
   wchar_t (&wcstr)[size],
   const char *mbstr,
   size_t count,
   _locale_t locale
); // C++ only
```

### <a name="parameters"></a>매개 변수

*wcstr*<br/>
와이드 문자 시퀀스의 주소입니다.

*mbstr*<br/>
null로 끝나는 멀티바이트 문자 시퀀스의 주소입니다.

*count*<br/>
변환할 멀티바이트 문자의 최대 수입니다.

*locale*<br/>
사용할 로캘입니다.

## <a name="return-value"></a>반환 값

하는 경우 **mbstowcs** 소스 문자열을 성공적으로 변환 변환 된 멀티 바이트 문자의 수를 반환 합니다. 경우는 *wcstr* 인수가 **NULL**, 필요한 크기 (와이드 문자)는 대상 문자열을 반환 합니다. 하는 경우 **mbstowcs** 잘못 된 멀티 바이트 문자를 발견 하면-1을 반환 합니다. 반환 값이 *개수*, 와이드 문자 문자열의 null로 종료 되었습니다.

> [!IMPORTANT]
> 되도록 *wcstr* 및 *mbstr* 겹치지 않는 올바르고 *개수* 올바르게 변환할 멀티 바이트 문자의 수를 반영 합니다.

## <a name="remarks"></a>설명

합니다 **mbstowcs** 함수는 최대 개수까지 변환 *개수* 가리키는 멀티 바이트 문자 *mbstr* 된 해당 와이드 문자의 문자열로 현재 로캘에 따라 결정 됩니다. 결과 와이드 문자 문자열에 표시 된 주소에 저장 *wcstr*합니다. 일련의 호출 결과 비슷합니다 [mbtowc](mbtowc-mbtowc-l.md)합니다. 하는 경우 **mbstowcs** 때나 그 전에 싱글 바이트 null 문자 ('\0')를 발견 *개수* 로 변환 하 고 null 문자를 와이드 문자 null 문자 (L'\ \0')를 중지 합니다. 따라서 와이드 문자 문자열에 *wcstr* 는 null 종료 null 문자를 변환 하는 동안 발생 하는 경우에 합니다. 시퀀스에서 가리키는 경우 *wcstr* 하 고 *mbstr* 겹치는 경우 동작이 정의 되지 않습니다. 합니다.

경우는 *wcstr* 인수가 **NULL**에 **mbstowcs** null 종결자를 포함 하지 않습니다 변환에서 초래 하는 와이드 문자 수를 반환 합니다. 올바른 값을 반환하려면 소스 문자열이 null로 끝나야 합니다. 결과 와이드 문자열이 null로 끝나야 하는 경우 반환된 값에 추가하세요.

경우는 *mbstr* 인수가 **NULL**, 이거나 *count* 는 > **INT_MAX**, 에설명된대로잘못된매개변수처리기가호출[ 매개 변수 유효성 검사](../../c-runtime-library/parameter-validation.md) 합니다. Errno로 설정 된 실행은 계속 하도록 허용 하는 경우 **EINVAL** 함수-1을 반환 합니다.

**mbstowcs** 모든 로캘 종속 동작에 현재 로캘을 사용 **_mbstowcs_l** 대신 전달 된 로캘을 사용 한다는 점을 제외 하 고는 동일 합니다. 자세한 내용은 [Locale](../../c-runtime-library/locale.md)을 참조하세요.

C++에서 이러한 함수는 보다 최신의 보안 대응 함수를 호출하는 템플릿 오버로드를 갖고 있습니다. 자세한 내용은 [Secure Template Overloads](../../c-runtime-library/secure-template-overloads.md)을 참조하세요.

## <a name="requirements"></a>요구 사항

|루틴에서 반환된 값|필수 헤더|
|-------------|---------------------|
|**mbstowcs**|\<stdlib.h>|
|**_mbstowcs_l**|\<stdlib.h>|

호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.

## <a name="example"></a>예제

```C
// crt_mbstowcs.c
// compile with: /W3
// illustrates the behavior of the mbstowcs function

#include <stdlib.h>
#include <stdio.h>
#include <locale.h>

int main( void )
{
    size_t size;
    int nChar = 2; // number of characters to convert
    int requiredSize;

    unsigned char    *pmbnull  = NULL;
    unsigned char    *pmbhello = NULL;
    char* localeInfo;

    wchar_t *pwchello = L"\x3042\x3043"; // 2 Hiragana characters
    wchar_t *pwc;

    /* Enable the Japanese locale and codepage */
    localeInfo = setlocale(LC_ALL, "Japanese_Japan.932");
    printf("Locale information set to %s\n", localeInfo);

    printf( "Convert to multibyte string:\n" );

    requiredSize = wcstombs( NULL, pwchello, 0); // C4996
    // Note: wcstombs is deprecated; consider using wcstombs_s
    printf("   Required Size: %d\n", requiredSize);

    /* Add one to leave room for the null terminator. */
    pmbhello = (unsigned char *)malloc( requiredSize + 1);
    if (! pmbhello)
    {
        printf("Memory allocation failure.\n");
        return 1;
    }
    size = wcstombs( pmbhello, pwchello, requiredSize + 1); // C4996
    // Note: wcstombs is deprecated; consider using wcstombs_s
    if (size == (size_t) (-1))
    {
        printf("Couldn't convert string. Code page 932 may"
                " not be available.\n");
        return 1;
    }
    printf( "   Number of bytes written to multibyte string: %u\n",
            (unsigned int) size );
    printf( "   Hex values of the" );
    printf( " multibyte characters: %#.2x %#.2x %#.2x %#.2x\n",
            pmbhello[0], pmbhello[1], pmbhello[2], pmbhello[3] );
    printf( "   Codepage 932 uses 0x81 to 0x9f as lead bytes.\n\n");

    printf( "Convert back to wide-character string:\n" );

    /* Assume we don't know the length of the multibyte string.
     Get the required size in characters, and allocate enough space. */

    requiredSize = mbstowcs(NULL, pmbhello, 0); // C4996
    /* Add one to leave room for the null terminator */
    pwc = (wchar_t *)malloc( (requiredSize + 1) * sizeof( wchar_t ));
    if (! pwc)
    {
        printf("Memory allocation failure.\n");
        return 1;
    }
    size = mbstowcs( pwc, pmbhello, requiredSize + 1); // C4996
    if (size == (size_t) (-1))
    {
       printf("Couldn't convert string--invalid multibyte character.\n");
    }
    printf( "   Characters converted: %u\n", (unsigned int)size );
    printf( "   Hex value of first 2" );
    printf( " wide characters: %#.4x %#.4x\n\n", pwc[0], pwc[1] );
    free(pwc);
    free(pmbhello);
}
```

```Output
Locale information set to Japanese_Japan.932
Convert to multibyte string:
   Required Size: 4
   Number of bytes written to multibyte string: 4
   Hex values of the  multibyte characters: 0x82 0xa0 0x82 0xa1
   Codepage 932 uses 0x81 to 0x9f as lead bytes.

Convert back to wide-character string:
   Characters converted: 2
   Hex value of first 2 wide characters: 0x3042 0x3043
```

## <a name="see-also"></a>참고자료

[데이터 변환](../../c-runtime-library/data-conversion.md)<br/>
[로캘](../../c-runtime-library/locale.md)<br/>
[멀티바이트 문자 시퀀스 해석](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)<br/>
[_mbclen, mblen, _mblen_l](mbclen-mblen-mblen-l.md)<br/>
[mbtowc, _mbtowc_l](mbtowc-mbtowc-l.md)<br/>
[wcstombs, _wcstombs_l](wcstombs-wcstombs-l.md)<br/>
[wctomb, _wctomb_l](wctomb-wctomb-l.md)<br/>
[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)<br/>
