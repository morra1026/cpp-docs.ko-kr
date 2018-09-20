---
title: 'Comptr:: Attach 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::ComPtr::Attach
dev_langs:
- C++
helpviewer_keywords:
- Attach method
ms.assetid: 5b911f2d-9830-4dc7-b9e3-527abd55d2c8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 0fcccf1c7816892a336839170a7a279f325b3f8b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46408273"
---
# <a name="comptrattach-method"></a>ComPtr::Attach 메서드

이 연결 **ComPtr** 현재 템플릿 형식 매개 변수에 의해 지정 된 인터페이스 형식을 사용 하 여 합니다.

## <a name="syntax"></a>구문

```cpp
void Attach(
   _In_opt_ InterfaceType* other
);
```

### <a name="parameters"></a>매개 변수

*other*<br/>
인터페이스 형식입니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[ComPtr 클래스](../windows/comptr-class.md)