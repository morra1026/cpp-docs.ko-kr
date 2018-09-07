---
title: _ASSERT, _ASSERTE, _ASSERT_EXPR 매크로 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
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
apitype: DLLExport
f1_keywords:
- _ASSERTE
- ASSERTE
- _ASSERT
- _ASSERT_EXPR
dev_langs:
- C++
helpviewer_keywords:
- debugging [CRT], using macros
- _ASSERTE macro
- macros, debugging with
- debug reporting macros
- _ASSERT macro
- _ASSERT_EXPR macro
ms.assetid: e98fd2a6-7f5e-4aa8-8fe8-e93490deba36
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 254550acf94acb846826bc0efe76ef26753c54b8
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44107592"
---
# <a name="assert-asserte-assertexpr-macros"></a>_ASSERT, _ASSERTE, _ASSERT_EXPR 매크로

식을 계산 하 고 결과 경우 디버그 보고서 생성 **False** (디버그 버전에만 해당).

## <a name="syntax"></a>구문

```C
// Typical usage:
_ASSERT_EXPR( booleanExpression, message );
_ASSERT( booleanExpression );
_ASSERTE( booleanExpression );
```

### <a name="parameters"></a>매개 변수

*booleanExpression*<br/>
0이 아닌 값(true) 또는 0(false)으로 계산되는 스칼라 식(포인터 식 포함)입니다.

*message*<br/>
보고서 일부로 표시할 전각 문자열입니다.

## <a name="remarks"></a>설명

합니다 **_ASSERT_EXPR**를 **_ASSERT** 하 고 **_ASSERTE** 매크로 디버깅 프로세스 중에 가정을 확인 하기 위한 단순한 메커니즘을 사용 하 여 응용 프로그램을 제공 합니다. 이들 매크로는 응용 프로그램의 정품 빌드 시 호출되지 않도록 `#ifdef` 문에 포함할 필요가 없으므로 매우 유연합니다. 이 유연성을 얻으려면 [_DEBUG](../../c-runtime-library/debug.md) 매크로를 사용합니다. **_ASSERT_EXPR**, **_ASSERT** 하 고 **_ASSERTE** 만 하면 볼 수 있습니다 **_DEBUG** 컴파일 타임에 정의 됩니다. 때 **_DEBUG** 가 정의 되지 않은 이러한 매크로 호출이 전처리 중 제거 됩니다.

**_ASSERT_EXPR**, **_ASSERT** 하 고 **_ASSERTE** 평가 자신의 *booleanExpression* 인수와 결과가 **false**(0), 호출을 진단 메시지 출력 [_CrtDbgReportW](crtdbgreport-crtdbgreportw.md) 디버그 보고서를 생성 합니다. 합니다 **_ASSERT** 매크로 간단한 진단 메시지를 출력 **_ASSERTE** 메시지에 실패 한 식의 문자열 표현을 포함 하 고 **_ASSERT_EXPR** 포함 된 *메시지* 진단 메시지의 문자열입니다. 이러한 매크로 아무것도 하지 때 *booleanExpression* 0이 아닌 값으로 계산 합니다.

**_ASSERT_EXPR**, **_ASSERT** 하 고 **_ASSERTE** 호출 **_CrtDbgReportW**, 와이드 문자에 모든 출력 합니다. **_ASSERTE** 유니코드 문자를 제대로 출력 *booleanExpression* 하 고 **_ASSERT_EXPR** 의 유니코드 문자를 출력 *메시지*합니다.

때문에 **_ASSERTE** 매크로 실패 한 식을 지정 및 **_ASSERT_EXPR** 있습니다를 참조 하지 않고 문제를 식별할 수 있도록, 생성된 된 보고서에 메시지를 지정 합니다 응용 프로그램 소스 코드입니다. 그러나 단점은 존재 하는 모든 *메시지* 하 여 인쇄 **_ASSERT_EXPR** 및 모든 식에 의해 평가 **_ASSERTE** 출력 (디버그 버전)에 포함 된 문자열 상수는 응용 프로그램의 파일입니다. 따라서 많은 수의 경우 호출할 **_ASSERT_EXPR** 또는 **_ASSERTE**, 해당이 식에서 출력 파일의 크기를 크게 증가할 수 있습니다.

[_CrtSetReportMode](crtsetreportmode.md) 및 [_CrtSetReportFile](crtsetreportfile.md) 함수를 사용해서 지정하지 않으면 메시지가 설정에 해당하는 팝업 대화 상자에 표시됩니다.

```C
_CrtSetReportMode(CRT_ASSERT, _CRTDBG_MODE_WNDW);
````

**_CrtDbgReportW** 디버그 보고서를 생성 하 고 해당 대상 또는 대상에는 현재 보고서 모드 및 파일에 대 한 정의에 따라 결정 합니다 **_CRT_ASSERT** 형식을 보고 합니다. 기본적으로 어설션 실패 및 오류는 디버그 메시지 창에 전달됩니다. [_CrtSetReportMode](crtsetreportmode.md) 및 [_CrtSetReportFile](crtsetreportfile.md) 함수는 각 보고서 종류의 대상을 정의하는 데 사용됩니다.

경우 대상이 디버그 메시지 창이 고 사용자가를 **다시 시도** 단추를 **_CrtDbgReportW** 1을 반환 합니다 발생 합니다 **_ASSERT_EXPR**, **_ ASSERT** 하 고 **_ASSERTE** 매크로가 시간 (JIT) 디버깅을 사용 하는 디버거를 시작 합니다.

보고 프로세스에 대한 자세한 내용은 [_CrtDbgReport, _CrtDbgReportW](crtdbgreport-crtdbgreportw.md) 함수를 참조하세요. 어설션 실패를 해결하고 이들 매크로를 디버깅 오류 처리 메커니즘으로 사용하는 방법에 대한 자세한 내용은 [확인 및 보고에 매크로 사용](/visualstudio/debugger/macros-for-reporting)을 참조하세요.

외에 **_ASSERT** 매크로 [assert](assert-macro-assert-wassert.md) 프로그램 논리를 확인 하려면 매크로 사용할 수 있습니다. 이 매크로는 라이브러리의 디버그 및 릴리스 버전에서 둘 다 사용할 수 있습니다. [_RPT, _RPTF](rpt-rptf-rptw-rptfw-macros.md) 디버그 매크로는 디버그 보고서 생성에도 사용할 수 있지만 식을 계산하지 않습니다. 합니다 **_RPT** 매크로 간단한 보고서를 생성 합니다. 합니다 **_RPTF** 매크로 생성된 된 보고서에 보고서 매크로 호출한 소스 파일과 줄 번호를 포함 합니다. 이러한 매크로의 와이드 문자 버전은 사용할 수 있습니다 (**_RPTW**하십시오 **_RPTFW**). 와이드 문자 문자열이 모든 문자열 매개 변수 및 출력에 사용된다는 점을 제외하고 와이드 문자 버전은 반각 문자 버전과 똑같습니다.

하지만 **_ASSERT_EXPR**를 **_ASSERT** 하 고 **_ASSERTE** 는 매크로 고 포함 하 여 사용할 \<crtdbg.h >, 응용 프로그램 디버그를 사용 하 여 연결 해야 합니다 C 런타임 라이브러리의 버전 때 **_DEBUG** 이러한 매크로 다른 런타임 함수를 호출 하기 때문에 정의 됩니다.

## <a name="requirements"></a>요구 사항

|매크로|필수 헤더|
|-----------|---------------------|
|**_ASSERT_EXPR**하십시오 **_ASSERT**, **_ASSERTE**|\<crtdbg.h>|

## <a name="example"></a>예제

이 프로그램에서 호출 하는 **_ASSERT** 하 고 **_ASSERTE** 조건을 테스트 하려면 매크로 `string1 == string2`. 조건이 실패하면 이들 매크로가 진단 메시지를 출력합니다. **_RPT** 및 **_RPTF** 매크로 그룹 하는 대신 실행이 프로그램에서는 또한 합니다 **printf** 함수입니다.

```C
// crt_ASSERT_macro.c
// compile with: /D_DEBUG /MTd /Od /Zi /link /verbose:lib /debug
//
// This program uses the _ASSERT and _ASSERTE debugging macros.
//

#include <stdio.h>
#include <string.h>
#include <malloc.h>
#include <crtdbg.h>

int main()
{
   char *p1, *p2;

   // The Reporting Mode and File must be specified
   // before generating a debug report via an assert
   // or report macro.
   // This program sends all report types to STDOUT.
   _CrtSetReportMode(_CRT_WARN, _CRTDBG_MODE_FILE);
   _CrtSetReportFile(_CRT_WARN, _CRTDBG_FILE_STDOUT);
   _CrtSetReportMode(_CRT_ERROR, _CRTDBG_MODE_FILE);
   _CrtSetReportFile(_CRT_ERROR, _CRTDBG_FILE_STDOUT);
   _CrtSetReportMode(_CRT_ASSERT, _CRTDBG_MODE_FILE);
   _CrtSetReportFile(_CRT_ASSERT, _CRTDBG_FILE_STDOUT);

   // Allocate and assign the pointer variables.
   p1 = (char *)malloc(10);
   strcpy_s(p1, 10, "I am p1");
   p2 = (char *)malloc(10);
   strcpy_s(p2, 10, "I am p2");

   // Use the report macros as a debugging
   // warning mechanism, similar to printf.
   // Use the assert macros to check if the
   // p1 and p2 variables are equivalent.
   // If the expression fails, _ASSERTE will
   // include a string representation of the
   // failed expression in the report.
   // _ASSERT does not include the
   // expression in the generated report.
   _RPT0(_CRT_WARN,
       "Use the assert macros to evaluate the expression p1 == p2.\n");
   _RPTF2(_CRT_WARN, "\n Will _ASSERT find '%s' == '%s' ?\n", p1, p2);
   _ASSERT(p1 == p2);

   _RPTF2(_CRT_WARN, "\n\n Will _ASSERTE find '%s' == '%s' ?\n",
          p1, p2);
   _ASSERTE(p1 == p2);

   _RPT2(_CRT_ERROR, "'%s' != '%s'\n", p1, p2);

   free(p2);
   free(p1);

   return 0;
}
```

```Output
Use the assert macros to evaluate the expression p1 == p2.
crt_ASSERT_macro.c(54) :
Will _ASSERT find 'I am p1' == 'I am p2' ?
crt_ASSERT_macro.c(55) : Assertion failed!
crt_ASSERT_macro.c(58) :

Will _ASSERTE find 'I am p1' == 'I am p2' ?
crt_ASSERT_macro.c(59) : Assertion failed: p1 == p2
'I am p1' != 'I am p2'
```

## <a name="see-also"></a>참고자료

[디버그 루틴](../../c-runtime-library/debug-routines.md)<br/>
[assert Macro, _assert, _wassert](assert-macro-assert-wassert.md)<br/>
[_RPT, _RPTF, _RPTW, _RPTFW 매크로](rpt-rptf-rptw-rptfw-macros.md)<br/>
