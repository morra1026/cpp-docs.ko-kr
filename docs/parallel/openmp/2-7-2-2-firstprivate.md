---
title: 2.7.2.2 firstprivate | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: ece6ff12-2be1-4e4f-866c-d39345fd87b5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0d3e6ad966f4cf895da9374798f6c9a4079ccc2f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46400967"
---
# <a name="2722-firstprivate"></a>2.7.2.2 firstprivate

합니다 **firstprivate** 절에서 제공 하는 기능의 상위 집합을 제공 합니다 **개인** 절. 구문의 합니다 **firstprivate** 절은 다음과 같습니다.

```
firstprivate(variable-list)
```

변수에서 지정한 *변수 목록* 있어야 **개인** 절 의미 체계를에 설명 된 대로 [2.7.2.1 섹션](../../parallel/openmp/2-7-2-1-private.md) 25 페이지. 초기화 또는 생성 구문 스레드의 실행 전에 스레드당 한 번 수행 하는 것 처럼 발생 합니다. 에 **firstprivate** 병렬 구문에서 절 새 개인 개체의 초기 값은이 발생 하는 스레드에 대 한 병렬 구문 직전 존재 하는 원래 개체의 값입니다. 에 **firstprivate** 절 작업 공유 구문에서 작업 공유 생성자를 실행 하는 각 스레드에 대 한 새 개인 개체의 초기 값이 시간에서 전에 존재 하는 원래 개체의 값을 동일한 스레드에서 작업 공유 생성자가 발생합니다. 또한 c + + 개체에 대 한 새 개인 각 스레드에 대해 개체가 원래 개체에서 복사 생성 합니다.

제한 된 **firstprivate** 절은 다음과 같습니다.

- 에 지정 된 변수를 **firstprivate** 불완전 한 형식 이거나 참조 형식 절이 없어야 합니다.

- 으로 지정 된 클래스 형식의 변수에 **firstprivate** 는 액세스 가능 하며 명확한 복사 생성자가 있어야 합니다.

- 병렬 영역 내부에서는 개인 또는에 표시 되는 변수를 **감소** 절을 **병렬** 지시문에 지정할 수 없습니다는 **firstprivate** 절에는 병렬 구문에 바인딩하는 작업 공유 지시문입니다.