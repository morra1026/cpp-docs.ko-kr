---
title: _bstr_t::copy | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _bstr_t::copy
dev_langs:
- C++
helpviewer_keywords:
- Copy method [C++]
- BSTR object [C++], copy
ms.assetid: 00ba7311-e82e-4a79-8106-5329fa2f869a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 50f9a17c93849dec49c2c9a72825a5797d8c040c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46068626"
---
# <a name="bstrtcopy"></a>_bstr_t::copy

**Microsoft 전용**

캡슐화된 `BSTR`의 복사본을 구성합니다.

## <a name="syntax"></a>구문

```
BSTR copy( bool fCopy = true ) const;
```

#### <a name="parameters"></a>매개 변수

*fCopy*<br/>
TRUE 이면 **복사본** 포함된 된 복사본을 반환 합니다 `BSTR`고, 그렇지 않으면 **복사** 는 실제 BSTR을 반환 합니다.

## <a name="remarks"></a>설명

캡슐화된 `BSTR` 개체에 새로 할당된 복사본을 반환합니다.

## <a name="example"></a>예제

```cpp
STDMETHODIMP CAlertMsg::get_ConnectionStr(BSTR *pVal){ //  m_bsConStr is _bstr_t
   *pVal = m_bsConStr.copy();
}
```

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_bstr_t 클래스](../cpp/bstr-t-class.md)