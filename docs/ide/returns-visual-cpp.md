---
title: '&lt;returns&gt;(Visual C++)'
ms.date: 11/04/2016
f1_keywords:
- returns
- <returns>
helpviewer_keywords:
- returns C++ XML tag
- <returns> C++ XML tag
ms.assetid: 5e3b0ed9-838d-4953-a93e-76d2d0a19fb9
ms.openlocfilehash: 7861d57d474db3c45b2c773a057a545c15602822
ms.sourcegitcommit: dedd4c3cb28adec3793329018b9163ffddf890a4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "57740851"
---
# <a name="ltreturnsgt-visual-c"></a>&lt;returns&gt;(Visual C++)

\<returns> 태그는 메서드 선언의 주석에서 반환 값을 설명하는 데 사용해야 합니다.

## <a name="syntax"></a>구문

```
<returns>description</returns>
```

#### <a name="parameters"></a>매개 변수

*description*<br/>
반환 값에 대한 설명입니다.

## <a name="remarks"></a>주의

[/doc](../build/reference/doc-process-documentation-comments-c-cpp.md)로 컴파일하여 문서 주석을 파일로 처리합니다.

## <a name="example"></a>예제

```
// xml_returns_tag.cpp
// compile with: /LD /clr /doc
// post-build command: xdcmake xml_returns_tag.dll

/// Text for class MyClass.
public ref class MyClass {
public:
   /// <returns>Returns zero.</returns>
   int GetZero() { return 0; }
};
```

## <a name="see-also"></a>참고 항목

[XML 문서](../ide/xml-documentation-visual-cpp.md)
