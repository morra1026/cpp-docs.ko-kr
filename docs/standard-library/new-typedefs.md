---
title: '&lt;new&gt; 형식 정의 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- new/std::new_handler
ms.assetid: aef01de1-06b5-4b6c-aebc-2c9f423d7e47
ms.openlocfilehash: bbfe7d2c24cb589925c70c70235f6de112d274f1
ms.sourcegitcommit: b92ca0b74f0b00372709e81333885750ba91f90e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/16/2018
ms.locfileid: "42543245"
---
# <a name="ltnewgt-typedefs"></a>&lt;new&gt; 형식 정의

| |
| - |
|[new_handler](#new_handler)|

## <a name="new_handler"></a>  new_handler

이 형식은 새 처리기로 사용하기에 적합한 함수를 가리킵니다.

```cpp
typedef void (*new_handler)();
```

### <a name="remarks"></a>설명

이 유형의 처리기 함수는 추가 저장소 요청을 충족할 수 없을 때 **operatornew** 또는 `operator new[]`에 의해 호출됩니다.

### <a name="example"></a>예

`new_handler`를 반환 값으로 사용하는 방법의 예제는 [set_new_handler](../standard-library/new-functions.md#set_new_handler)를 참조하세요.

## <a name="see-also"></a>참고자료

[\<new>](../standard-library/new.md)<br/>
