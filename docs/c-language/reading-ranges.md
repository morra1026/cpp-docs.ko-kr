---
title: 범위 읽기
ms.date: 11/04/2016
ms.assetid: 99de29ce-ab14-46f4-97e1-2081fd996b53
ms.openlocfilehash: b5c6a6baf43b8786fbd0301e4b89ea856d839606
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50604109"
---
# <a name="reading-ranges"></a>범위 읽기

**ANSI 4.9.6.2** `fscanf` 함수에서 % [ 변환을 위한 scanlist의 첫 번째 문자도 아니고 마지막 문자도 아닌 대시(–) 문자의 해석

다음 줄

```
fscanf( fileptr, "%[A-Z]", strptr);
```

에서는 A–Z 범위에 속한 문자의 개수를 `strptr`이 가리키는 문자열로 읽습니다.

## <a name="see-also"></a>참고 항목

[라이브러리 함수](../c-language/library-functions.md)