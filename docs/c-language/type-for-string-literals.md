---
title: 문자열 리터럴의 형식
ms.date: 11/04/2016
helpviewer_keywords:
- string literals, type
- types [C], string literals
ms.assetid: f50a28af-20c1-4440-bdc6-564c86a309c8
ms.openlocfilehash: 7e832ac7aa08ad80ab395baa59eabbabb486b46f
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152276"
---
# <a name="type-for-string-literals"></a>문자열 리터럴의 형식

문자열 리터럴은 `char` 배열(즉, **char[ ]**) 형식입니다. 와이드 문자 문자열은 `wchar_t` 배열(즉, **wchar_t[ ]**) 형식입니다. 즉, 문자열은 `char` 형식의 요소가 포함된 배열입니다. 배열에 있는 요소의 수는 문자열의 문자 개수에 null 종결 문자에 해당하는 1을 더한 값입니다.

## <a name="see-also"></a>참고 항목

[C 문자열 리터럴](../c-language/c-string-literals.md)
