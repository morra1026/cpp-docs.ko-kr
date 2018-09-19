---
title: _bstr_t::Attach | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _bstr_t::Attach
dev_langs:
- C++
helpviewer_keywords:
- Attach method [C++]
ms.assetid: 8cad867e-40fc-435b-841f-0d412c2f58d3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1eddbc7a01be66430759bb84c3ce6d840f37d098
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46111214"
---
# <a name="bstrtattach"></a>_bstr_t::Attach

**Microsoft 전용**

`_bstr_t` 래퍼를 `BSTR`에 연결합니다.

## <a name="syntax"></a>구문

```
void Attach(
   BSTR s
);
```

#### <a name="parameters"></a>매개 변수

*s*<br/>
`BSTR` 변수와 연결되거나 이 변수에 할당될 `_bstr_t`입니다.

## <a name="remarks"></a>설명

이전에 `_bstr_t`가 다른 `BSTR`에 연결된 경우 다른 `_bstr_t` 변수가 `BSTR`을 사용하고 있지 않으면 `_bstr_t`가 `BSTR` 리소스를 정리합니다.

## <a name="example"></a>예제

참조 [_bstr_t:: assign](../cpp/bstr-t-assign.md) 사용 하는 예제 **연결**합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_bstr_t 클래스](../cpp/bstr-t-class.md)