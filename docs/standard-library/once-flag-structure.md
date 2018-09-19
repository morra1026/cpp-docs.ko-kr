---
title: once_flag 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 09/17/2018
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- mutex/std::once_flag
dev_langs:
- C++
ms.assetid: 71bfb88d-ca8c-4082-a6e1-ff52151e8629
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 67cfbe06461598fbd04e124629399baa63fdd5d9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46104337"
---
# <a name="onceflag-structure"></a>once_flag 구조체

나타냅니다는 **구조체** 템플릿 함수를 사용 하 여 사용 되는 [call_once](../standard-library/mutex-functions.md#call_once) 해당 초기화 되도록 코드는 한 번만 호출, 다중 스레드 방식의 실행 하는 경우에 합니다.

## <a name="syntax"></a>구문

구조체 once_flag {constexpr once_flag() noexcept;};

## <a name="remarks"></a>설명

합니다 `once_flag` **구조체** 기본 생성자만 포함 합니다.

`once_flag` 형식의 개체는 만들 수는 있지만 복사할 수는 없습니다.

## <a name="requirements"></a>요구 사항

**헤더:** \<뮤텍스 >

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)<br/>
[\<mutex>](../standard-library/mutex.md)<br/>
