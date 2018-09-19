---
title: _com_error::HRESULTToWCode | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_error::HRESULTToWCode
dev_langs:
- C++
helpviewer_keywords:
- HRESULTToWCode method [C++]
ms.assetid: ff3789f5-1047-41a0-b7e3-86dd8f638dba
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c39b638451aa8ea89191e323eae5f2c140563990
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46082068"
---
# <a name="comerrorhresulttowcode"></a>_com_error::HRESULTToWCode

**Microsoft 전용**

16 비트에서 32 비트 HRESULT 매핑됩니다 `wCode`합니다.

## <a name="syntax"></a>구문

```
static WORD HRESULTToWCode(
   HRESULT hr
) throw( );
```

#### <a name="parameters"></a>매개 변수

*hr*<br/>
16 비트와 매핑되어야 32 비트 HRESULT `wCode`합니다.

## <a name="return-value"></a>반환 값

16 비트 `wCode` 32 비트 HRESULT에서 매핑됩니다.

## <a name="remarks"></a>설명

참조 [_com_error:: wcode](../cpp/com-error-wcode.md) 자세한 내용은 합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[_com_error::WCode](../cpp/com-error-wcode.md)<br/>
[_com_error::WCodeToHRESULT](../cpp/com-error-wcodetohresult.md)<br/>
[_com_error 클래스](../cpp/com-error-class.md)