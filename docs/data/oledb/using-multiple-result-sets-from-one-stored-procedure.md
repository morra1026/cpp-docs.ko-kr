---
title: 저장 프로시저 하나에서 여러 결과 집합 사용 | Microsoft Docs
ms.custom: ''
ms.date: 10/24/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- stored procedures, returning result sets
- multiple result sets
ms.assetid: c450c12c-a76c-4ae4-9675-071a41eeac05
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: ac30f74a593f79cea7f252c454f19b85260e27b8
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50078515"
---
# <a name="using-multiple-result-sets-from-one-stored-procedure"></a>저장 프로시저 하나에서 여러 결과 집합 사용

대부분의 저장된 프로시저는 여러 결과 집합을 반환 합니다. 자세한 내용은 select 문 또는 일반적으로 이러한 저장된 프로시저가 하나 포함 됩니다. 소비자가이 포함 된 모든 결과 집합을 처리 하는 것이 좋습니다.

## <a name="to-handle-multiple-result-sets"></a>여러 결과 처리 하도록 설정 합니다.

1. 만들기는 `CCommand` 클래스와 `CMultipleResults` 템플릿 인수로 및 선택한 일반적으로 동적 또는 수동 접근자의 접근자와 함께 합니다. 다른 유형의 접근자를 사용 하는 경우 각 행 집합에 대 한 출력 열을 결정할 수 수 없습니다.

1. 일반적으로 저장된 프로시저를 실행 하 고 열 바인딩 (참조 [방법 데이터 페치?](../../data/oledb/fetching-data.md)).

1. 데이터를 사용 합니다.

1. 호출 `GetNextResult` 에 `CCommand` 클래스입니다. 다른 결과 행 집합을 사용할 수 있으면 `GetNextResult` S_OK를 반환 및 수동 접근자를 사용 하는 경우 열에 바인딩해야 합니다. 경우 `GetNextResult` 오류가 반환 가지 다음 결과 집합이 더 이상 사용할 수 있습니다.

## <a name="see-also"></a>참고 항목

[저장 프로시저 사용](../../data/oledb/using-stored-procedures.md)