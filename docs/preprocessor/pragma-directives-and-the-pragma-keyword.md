---
title: Pragma 지시문 및 __Pragma 키워드
ms.date: 11/04/2016
f1_keywords:
- '#pragma'
helpviewer_keywords:
- '#pragma directives, C/C++'
- __pragma keyword
- pragma directives, C/C++
- pragmas, C/C++
- preprocessor
- pragmas
- preprocessor, pragmas
- pragma directives (#pragma)
ms.assetid: 9867b438-ac64-4e10-973f-c3955209873f
ms.openlocfilehash: 9e79ba7378e28fdea863af010decb7064df415cd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50660098"
---
# <a name="pragma-directives-and-the-pragma-keyword"></a>Pragma 지시문 및 __Pragma 키워드

Pragma 지시문이 컴퓨터 또는 운영 체제 관련 컴파일러 기능을 지정합니다. 합니다 **__pragma** Microsoft 컴파일러에만 해당 되는 키워드를 매크로 정의 안에 pragma 지시문을 코드에 있습니다.

## <a name="syntax"></a>구문

```
#pragma token-string
__pragma(token-string)
```

## <a name="remarks"></a>설명

C 및 C++의 각 구현은 호스트 컴퓨터나 운영 체제에 고유한 기능을 몇 가지 지원합니다. 예를 들어, 일부 프로그램은 데이터가 저장되는 메모리 영역을 정확하게 제어하거나 특정 함수가 매개 변수를 수신하는 방법을 제어해야 합니다. 합니다 **#pragma** 지시문 C 및 c + + 언어와 전반적인 호환성을 유지 하면서 컴파일러가 컴퓨터 및 운영 체제 관련 기능에 대 한 방법을 제공 합니다.

Pragma는 정의에 따라 컴퓨터 전용이거나 운영 체제 전용이며 대개 컴파일러마다 다릅니다. Pragma를 조건문에 사용하여 새로운 전처리기 기능을 제공하거나 구현 정의 정보를 컴파일러에 제공할 수 있습니다.

`token-string`은 특정 컴파일러 명령과 인수를 제공하는(있을 경우) 일련의 문자입니다. 숫자 기호 (**#**) 첫 번째 공백이 아닌 문자 여야 합니다. 줄에 포함 하는 pragma; 공백 문자는 숫자 기호와 단어 "pragma" 구분할 수 있습니다. 다음 **#pragma**, 변환기가 전처리 토큰으로 구문 분석할 수 있는 모든 텍스트를 작성 합니다. 인수 **#pragma** 매크로 확장 될 수 있습니다.

컴파일러가 인식할 수 없는 pragma를 찾으면 경고를 표시하고 컴파일을 계속합니다.

Microsoft C 및 C++ 컴파일러는 다음 pragma를 인식합니다.

||||
|-|-|-|
|[alloc_text](../preprocessor/alloc-text.md)|[auto_inline](../preprocessor/auto-inline.md)|[bss_seg](../preprocessor/bss-seg.md)|
|[check_stack](../preprocessor/check-stack.md)|[code_seg](../preprocessor/code-seg.md)|[comment](../preprocessor/comment-c-cpp.md)|
|[component](../preprocessor/component.md)|[conform](../preprocessor/conform.md) <sup>1</sup>|[const_seg](../preprocessor/const-seg.md)|
|[data_seg](../preprocessor/data-seg.md)|[deprecated](../preprocessor/deprecated-c-cpp.md)|[detect_mismatch](../preprocessor/detect-mismatch.md)|
|[fenv_access](../preprocessor/fenv-access.md)|[float_control](../preprocessor/float-control.md)|[fp_contract](../preprocessor/fp-contract.md)|
|[function](../preprocessor/function-c-cpp.md)|[hdrstop](../preprocessor/hdrstop.md)|[include_alias](../preprocessor/include-alias.md)|
|[init_seg](../preprocessor/init-seg.md) <sup>1</sup>|[inline_depth](../preprocessor/inline-depth.md)|[inline_recursion](../preprocessor/inline-recursion.md)|
|[intrinsic](../preprocessor/intrinsic.md)|[loop](../preprocessor/loop.md) <sup>1</sup>|[make_public](../preprocessor/make-public.md)|
|[managed](../preprocessor/managed-unmanaged.md)|[message](../preprocessor/message.md)||
|[omp](../preprocessor/omp.md)|[once](../preprocessor/once.md)||
|[optimize](../preprocessor/optimize.md)|[pack](../preprocessor/pack.md)|[pointers_to_members](../preprocessor/pointers-to-members.md) <sup>1</sup>|
|[pop_macro](../preprocessor/pop-macro.md)|[push_macro](../preprocessor/push-macro.md)|[region, endregion](../preprocessor/region-endregion.md)|
|[runtime_checks](../preprocessor/runtime-checks.md)|[section](../preprocessor/section.md)|[setlocale](../preprocessor/setlocale.md)|
|[strict_gs_check](../preprocessor/strict-gs-check.md)|[unmanaged](../preprocessor/managed-unmanaged.md)|[vtordisp](../preprocessor/vtordisp.md) <sup>1</sup>|
|[warning](../preprocessor/warning.md)|||

<sup>1</sup> c + + 컴파일러 에서만 지원 됩니다.

## <a name="pragmas-and-compiler-options"></a>Pragma 및 컴파일러 옵션

일부 pragma는 컴파일러 옵션과 같은 기능을 제공합니다. 소스 코드에 pragma가 발생하면 컴파일러 옵션에 지정된 동작을 재정의합니다. 예를 들어 지정한 [/zp8](../build/reference/zp-struct-member-alignment.md)를 사용 하 여 코드의 특정 섹션에 대 한이 컴파일러 설정을 재정의할 수 있습니다 [팩](../preprocessor/pack.md):

```
cl /Zp8 ...

<file> - packing is 8
// ...
#pragma pack(push, 1) - packing is now 1
// ...
#pragma pack(pop) - packing is 8
</file>
```

## <a name="the-pragma-keyword"></a>__pragma() 키워드

**Microsoft 전용**

컴파일러도 지원 합니다 **__pragma** 기능이 같은 키워드를으로 **#pragma** 지시문 매크로 정의에서 인라인으로 사용할된 수 있지만. 합니다 **#pragma** 컴파일러 되도록 지시문의 숫자 기호 문자 ('#')를 해석 하기 때문에 매크로 정의에서 지시문을 사용할 수 없습니다는 [문자열 화 연산자 (#)](../preprocessor/stringizing-operator-hash.md)합니다.

다음 코드 예제에서는 하는 방법을 **__pragma** 매크로에서 키워드를 사용할 수 있습니다. 이 코드는 "컴파일러 COM 지원 샘플"의 ACDUAL 샘플에 있는 mfcdual.h 헤더에서 발췌되었습니다.

```cpp
#define CATCH_ALL_DUAL \
CATCH(COleException, e) \
{ \
_hr = e->m_sc; \
} \
AND_CATCH_ALL(e) \
{ \
__pragma(warning(push)) \
__pragma(warning(disable:6246)) /*disable _ctlState prefast warning*/ \
AFX_MANAGE_STATE(pThis->m_pModuleState); \
__pragma(warning(pop)) \
_hr = DualHandleException(_riidSource, e); \
} \
END_CATCH_ALL \
return _hr; \
```

**End Microsoft 전용**

## <a name="see-also"></a>참고 항목

[ 전처리기 참조](../preprocessor/c-cpp-preprocessor-reference.md)<br/>
[C Pragma](../c-language/c-pragmas.md)<br/>
[키워드](../cpp/keywords-cpp.md)