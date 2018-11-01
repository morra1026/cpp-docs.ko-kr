---
title: 컬렉션 및 열거자 인터페이스 (ATL) 디자인
ms.date: 11/04/2016
helpviewer_keywords:
- enumerator interfaces
- collection interfaces
ms.assetid: ea19a39e-6333-41a1-be62-5435c236640e
ms.openlocfilehash: 8c7f782f52391b162a8b32a97961269178999ee0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50538205"
---
# <a name="design-principles-for-collection-and-enumerator-interfaces"></a>컬렉션 및 열거자 인터페이스에 대 한 디자인 원칙

각 유형의 인터페이스의 다양 한 디자인 원칙 가지가 있습니다.

- 컬렉션 인터페이스를 제공 *임의* 에 대 한 액세스를 *single* 를 통해 컬렉션의 항목을 `Item` 메서드를 통해 컬렉션에 있는 항목 수를 알 수 있습니다는 `Count` 속성, 종종 클라이언트 항목을 추가 및 제거할 수 있습니다.

- 열거자 인터페이스를 제공 *직렬* 에 대 한 액세스 *여러* 컬렉션의 항목을 클라이언트 검색 (중지 될 때까지 열거자 반환 컬렉션에 있는 항목 수를 허용 하지 않습니다 항목)을 추가 또는 제거 항목 전혀 제공 하지 않습니다.

인터페이스의 각 형식 컬렉션의 요소에 대 한 액세스를 제공 하는 다른 역할을 재생 합니다.

## <a name="see-also"></a>참고 항목

[컬렉션 및 열거자](../atl/atl-collections-and-enumerators.md)

