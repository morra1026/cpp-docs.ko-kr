---
title: '&lt;c&gt;(Visual C++)'
ms.date: 11/04/2016
f1_keywords:
- <c>
helpviewer_keywords:
- <c> C++ XML tag
- c C++ XML tag
ms.assetid: 3b23fc0f-e10d-4dd0-b197-48a46cbddd9f
ms.openlocfilehash: a5eb88be4cb5be8c4e970c285bad712093fdbb51
ms.sourcegitcommit: dedd4c3cb28adec3793329018b9163ffddf890a4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "57742596"
---
# <a name="ltcgt-visual-c"></a>&lt;c&gt;(Visual C++)

\<c> 태그는 설명 내 텍스트를 코드로 표시해야 함을 나타냅니다. 여러 줄을 코드로 지정하려면 [\<code>](../ide/code-visual-cpp.md)를 사용합니다.

## <a name="syntax"></a>구문

```
<c>text</c>
```

#### <a name="parameters"></a>매개 변수

*텍스트*<br/>
코드로 표시하려는 텍스트입니다.

## <a name="remarks"></a>주의

[/doc](../build/reference/doc-process-documentation-comments-c-cpp.md)로 컴파일하여 문서 주석을 파일로 처리합니다.

## <a name="example"></a>예제

```cpp
// xml_c_tag.cpp
// compile with: /doc /LD
// post-build command: xdcmake xml_c_tag.xdc

/// Text for class MyClass.
class MyClass {
public:
   int m_i;
   MyClass() : m_i(0) {}

   /// <summary><c>MyMethod</c> is a method in the <c>MyClass</c> class.
   /// </summary>
   int MyMethod(MyClass * a) {
      return a -> m_i;
   }
};
```

## <a name="see-also"></a>참고 항목

[XML 문서](../ide/xml-documentation-visual-cpp.md)
