---
title: 컴파일러 오류 C3072
ms.date: 11/04/2016
f1_keywords:
- C3072
helpviewer_keywords:
- C3072
ms.assetid: cdd5cb6b-c478-4698-adfa-c40188d34a18
ms.openlocfilehash: 34b5cff9191814b2a16a42d9e234bab09f29c117
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50490027"
---
# <a name="compiler-error-c3072"></a>컴파일러 오류 C3072

' operator '연산자는 ref 클래스의 인스턴스에 적용할 수 없습니다.

단항을 사용 하 여 '`operator` ' 연산자는 ref 클래스의 인스턴스를 핸들 형식으로 변환

CLR 형식 CLR 연산자, not 네이티브 (또는 표준) 연산자가 필요 합니다.  자세한 내용은 [추적 참조 연산자](../../windows/tracking-reference-operator-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3072를 생성합니다.

```
// C3072.cpp
// compile with: /clr
ref class R {};

int main() {
   R r1;
   R^ r2 = &r1;   // C3072
   R^ r3 = %r1;   // OK
}
```