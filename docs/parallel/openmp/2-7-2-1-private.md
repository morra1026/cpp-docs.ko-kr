---
title: 2.7.2.1 개인 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 079b4b84-f2b3-4050-a0ac-289493c36b3d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d06650a784b5b59405f446f4701918393b21fa3b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46387239"
---
# <a name="2721-private"></a>2.7.2.1 private

`private` 절은 팀에서 각 스레드에 private 일 변수 목록에서 변수를 선언 합니다. 구문의 `private` 절은 다음과 같습니다.

```
private(variable-list)
```

에 지정 된 변수 동작을 `private` 절은 다음과 같습니다. 구문에 대 한 자동 저장 기간이 있는 새 개체를 할당 됩니다. 크기 및 새 개체의 맞춤 변수 유형에 의해 결정 됩니다. 이 할당이 팀의 각 스레드에 대해 한 번 발생 하 고 기본 생성자가 호출 하 고 필요한 경우 클래스 개체에 대 한 그렇지 않은 경우 초기 값 확정적이 지 않습니다.  변수에서 참조 하는 원래 개체 구문에 진입할 때 비활성화 상태 값, 해당 구문의 동적 범위 내에서 수정 해서는 안 및 구문에서 종료 시 비활성화 상태 값입니다.

지시문 구문의 어휘 범위 내에서 변수는 스레드에 의해 할당 된 새 개인 개체를 참조 합니다.

제한 된 `private` 절은 다음과 같습니다.

- 에 지정 된 클래스 형식의 변수에 `private` 절에는 액세스 가능 하며 명확한 기본 생성자가 있어야 합니다.

- 에 지정 된 변수를 `private` 절이 없어야 합니다는 **const**-유형과 클래스에 없는 경우 형식 정규화를 `mutable` 멤버입니다.

- 에 지정 된 변수는 `private` 불완전 한 형식 이거나 참조 형식 절이 없어야 합니다.

- 에 표시 되는 변수를 `reduction` 절을 **병렬** 지시문에 지정할 수는 `private` 병렬 구문에 바인딩하는 작업 공유 지시문의 절.