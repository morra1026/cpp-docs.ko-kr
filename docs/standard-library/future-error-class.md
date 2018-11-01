---
title: future_error 클래스
ms.date: 11/04/2016
f1_keywords:
- future/std::future_error
ms.assetid: 6071c545-ac2a-49ef-9967-07b0125da861
ms.openlocfilehash: 2b3f754c0ceb7384d99c6a657de214d30aca24b3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50430475"
---
# <a name="futureerror-class"></a>future_error 클래스

[future](../standard-library/future-class.md) 개체를 관리하는 형식의 메서드에서 throw될 수 있는 예외 개체를 설명합니다.

## <a name="syntax"></a>구문

```cpp
class future_error : public logic_error {
public:
    future_error(error_code code);

const error_code& code() const throw();

const char *what() const throw();

};
```

## <a name="requirements"></a>요구 사항

**헤더:** \<향후 >

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)<br/>
[logic_error 클래스](../standard-library/logic-error-class.md)<br/>
[error_code 클래스](../standard-library/error-code-class.md)<br/>
