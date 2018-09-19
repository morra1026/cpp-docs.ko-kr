---
title: 링커 도구 오류 LNK2033 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK2033
dev_langs:
- C++
helpviewer_keywords:
- LNK2033
ms.assetid: d61db467-9328-4788-bf54-e2a20537f13f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a6c547b4d35e2e7fe057cdd67f0dad47f58d000c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039996"
---
# <a name="linker-tools-error-lnk2033"></a>링커 도구 오류 LNK2033

'type'에 대 한 확인 되지 않은 typeref 토큰 (토큰)

형식을은 MSIL 메타 데이터의 정의가 없습니다.

LNK2033로 컴파일하는 경우 발생할 수 있습니다 **/clr: safe** 형식을 MSIL 모듈에서 참조 되는 위치는 MSIL 모듈의 형식에 대 한 정방향 선언에만 있습니다.

형식에서 정의 해야 **/clr: safe**합니다.

자세한 내용은 [/clr(공용 언어 런타임 컴파일)](../../build/reference/clr-common-language-runtime-compilation.md)을 참조하세요.

## <a name="example"></a>예제

다음 샘플 LNK2033를 생성합니다.

```
// LNK2033.cpp
// compile with: /clr:safe
// LNK2033 expected
ref class A;
ref class B {};

int main() {
   A ^ aa = nullptr;
   B ^ bb = nullptr;   // OK
};
```