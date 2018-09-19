---
title: 링커 도구 경고 LNK4253 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4253
dev_langs:
- C++
helpviewer_keywords:
- LNK4253
ms.assetid: ec7433a9-aa9c-495a-a9f2-075e7bc3e7bc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d26d688825f504cbce8224adc9a5766a555d2fc8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016821"
---
# <a name="linker-tools-warning-lnk4253"></a>링커 도구 경고 LNK4253

섹션 '사항 구역 1' 'section2;'에 병합 되지 않았습니다 'section3'에 이미 병합

충돌 하는 병합 요청 링커 여러 검색 합니다. 링커는 요청 중 하나를 무시 합니다.

A **/MERGE** 옵션 또는 지시문 및 `from` 섹션은 이미 이전 인해 다른 섹션에 병합 되었습니다 **병합/** 옵션 또는 지시문 (또는에서 암시적 병합으로 인해 링커)입니다.

LNK4253를 해결 하려면 병합 요청 중 하나를 제거 합니다.

X86을 대상으로 할 때 컴퓨터 및 Visual c + +를 사용 하 여 Windows CE 대상 (ARM, MIPS, SH4, 및 엄지 단추) 합니다. CRT 섹션 읽기 전용 이제입니다. 코드는 이전 동작에 의존 하는 경우 (합니다. CRT 섹션은 읽기/쓰기), 예기치 않은 동작을 볼 수 있습니다.

자세한 내용은 다음 항목을 참조하세요.

- [/MERGE(섹션 결합)](../../build/reference/merge-combine-sections.md)

- [C 주석(C/C++)](../../preprocessor/comment-c-cpp.md)

## <a name="example"></a>예제

다음 샘플에서는 링커가 병합 하도록 지시 합니다 `.rdata` 섹션을 두 번 서로 다른 섹션에 있습니다. 다음 샘플 LNK4253를 생성합니다.

```
// LNK4253.cpp
// compile with: /W1 /link /merge:.rdata=text2
// LNK4253 expected
#pragma comment(linker, "/merge:.rdata=.text")
int main() {}
```