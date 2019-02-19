---
title: char 형식
ms.date: 11/04/2016
helpviewer_keywords:
- type char
- unsigned char keyword [C]
- char keyword [C]
ms.assetid: a5da0866-e780-4793-be87-15a8426e7ea0
ms.openlocfilehash: bc8d3bef85b82d5bb5c2575b3bc6c6d8a4887140
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152211"
---
# <a name="type-char"></a>char 형식

`char` 형식은 표현할 수 있는 문자 집합 멤버의 정수 값을 저장하는 데 사용됩니다. 해당 정수 값은 지정된 문자에 대응하는 ASCII 코드입니다.

**Microsoft 전용**

`unsigned char` 형식의 문자 값 범위는 0에서 0xFF까지의 16 진수입니다. **signed char**의 범위는 0x80에서 0x7F까지입니다. 이 범위는 0에서 255까지의 10진수 및 -128에서 +127까지의 10진수로 각각 변환됩니다. /J 컴파일러 옵션은 기본값을 **signed**에서 `unsigned`로 변경합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[기본 형식의 스토리지](../c-language/storage-of-basic-types.md)
