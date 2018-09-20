---
title: SafeCast | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- SafeCast
dev_langs:
- C++
helpviewer_keywords:
- SafeCast function
ms.assetid: 55316729-8456-403a-9f96-59d4038f67af
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 65794dafe5e45cbd4c0e2a7eb49c34377009deee
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46392985"
---
# <a name="safecast"></a>SafeCast

한 가지 형식의 숫자를 다른 형식으로 캐스팅합니다.

## <a name="syntax"></a>구문

```cpp
template<typename T, typename U>
inline bool SafeCast (
   const T From,
   U& To
);
```

### <a name="parameters"></a>매개 변수

*From*<br/>
[in] 변환할 원본 숫자입니다. 이 형식 이어야 합니다 `T`합니다.

*대상*<br/>
[out] 새 숫자 형식에 대 한 참조입니다. 이 형식 이어야 합니다 `U`합니다.

## <a name="return-value"></a>반환 값

**true** 오류가 발생 하지 않으면; **false** 오류가 발생 합니다.

## <a name="remarks"></a>설명

이 메서드는 부분 [SafeInt 라이브러리](../windows/safeint-library.md) 의 인스턴스를 만들지 않고 단일 캐스팅 작업을 위해 설계 되었습니다 합니다 [SafeInt 클래스](../windows/safeint-class.md)합니다.

> [!NOTE]
> 이 메서드는 단일 작업을 보호 해야 하는 경우에 사용 해야 합니다. 작업이 여러 개 있으면 개별 독립 실행형 함수를 호출하는 대신 `SafeInt` 클래스를 사용해야 합니다.

템플릿 형식 T 및 U에 대 한 자세한 내용은 참조 하세요. [SafeInt 함수](../windows/safeint-functions.md)합니다.

## <a name="requirements"></a>요구 사항

**헤더:** safeint.h

**Namespace:** microsoft:: utilities

## <a name="see-also"></a>참고 항목

[SafeInt 함수](../windows/safeint-functions.md)<br/>
[SafeInt 라이브러리](../windows/safeint-library.md)<br/>
[SafeInt 클래스](../windows/safeint-class.md)