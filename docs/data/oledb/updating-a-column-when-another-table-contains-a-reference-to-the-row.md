---
title: 다른 테이블의 행에 대 한 참조를 포함 하는 경우 열을 업데이트할 | Microsoft Docs
ms.custom: ''
ms.date: 10/24/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- rowsets, column updates
ms.assetid: abb5db69-055d-431f-b12d-ad2940a661ba
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 7998897c80e392326213324804c1809656e051f3
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50071825"
---
# <a name="updating-a-column-when-another-table-contains-a-reference-to-the-row"></a>다른 테이블에 행에 대한 참조가 들어 있는 경우의 열 업데이트

일부 공급자는 행 변경 내용이 열을 검색할 수 있지만 대부분의 공급자 수 없습니다. 결과적으로, 업데이트 하고자 하는 행에 대 한 참조가 있을 때 열을 업데이트 하면 오류가 발생할 수 있습니다. 이 문제를 해결 하려면 변경 하려는 열만 보유 하는 별도 접근자를 만듭니다. 해당 접근자의 번호를 전달 `SetData`합니다.

## <a name="see-also"></a>참고 항목

[접근자 사용](../../data/oledb/using-accessors.md)