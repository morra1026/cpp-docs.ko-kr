---
title: 주소 스토리지
ms.date: 11/04/2016
helpviewer_keywords:
- storage [C++], addresses
- addresses [C++], storage of
ms.assetid: 423b2402-b847-4788-ad70-943b7c9c5c8b
ms.openlocfilehash: 47b09ab6cd0b2045206daaee4badad32858ff934
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56148740"
---
# <a name="storage-of-addresses"></a>주소 스토리지

주소에 필요한 스토리지의 크기 및 주소의 의미는 컴파일러의 구현에 따라 다릅니다. 다른 형식에 대한 포인터가 동일한 길이가 되도록 보장되지 않습니다. 따라서 **sizeof(char \*)** 가 **sizeof(int \*)** 와 반드시 일치하는 것은 아닙니다.

**Microsoft 전용**

Microsoft C 컴파일러의 경우 **sizeof(char \*)** 는 **sizeof(int \*)** 와 일치합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[포인터 선언](../c-language/pointer-declarations.md)
