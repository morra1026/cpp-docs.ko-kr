---
title: ConvertBSTRToString | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- ConvertBSTRToString
dev_langs:
- C++
helpviewer_keywords:
- ConvertBSTRToString function
ms.assetid: ab6ce555-3d75-4e9c-9cb8-ada6d8ce43b1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c46ab493c6f3c80d9bee4b4b0c04d9569c12e23c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075886"
---
# <a name="convertbstrtostring"></a>ConvertBSTRToString

**Microsoft 전용**

변환 된 `BSTR` 값을 `char *`.

## <a name="syntax"></a>구문

```
char* __stdcall ConvertBSTRToString(BSTR pSrc);
```

#### <a name="parameters"></a>매개 변수

*pSrc*<br/>
BSTR 변수입니다.

## <a name="remarks"></a>설명

**ConvertBSTRToString** 삭제 해야 하는 문자열을 할당 합니다.

## <a name="example"></a>예제

```cpp
// ConvertBSTRToString.cpp
#include <comutil.h>
#include <stdio.h>

#pragma comment(lib, "comsuppw.lib")

int main() {
   BSTR bstrText = ::SysAllocString(L"Test");
   wprintf_s(L"BSTR text: %s\n", bstrText);

   char* lpszText2 = _com_util::ConvertBSTRToString(bstrText);
   printf_s("char * text: %s\n", lpszText2);

   SysFreeString(bstrText);
   delete[] lpszText2;
}
```

```Output
BSTR text: Test
char * text: Test
```

**Microsoft 전용 종료**

## <a name="requirements"></a>요구 사항

**헤더:** \<comutil.h >

**Lib:** comsuppw.lib 또는 comsuppwd.lib (참조 [/zc: wchar_t (wchar_t는 네이티브 형식임)](../build/reference/zc-wchar-t-wchar-t-is-native-type.md) 자세한)

## <a name="see-also"></a>참고자료

[컴파일러 COM 전역 함수](../cpp/compiler-com-global-functions.md)