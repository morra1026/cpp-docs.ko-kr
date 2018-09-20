---
title: 2.8 지시문 바인딩 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 7bdac45e-ab55-42f0-bd47-a2e3d5bbab3e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: dc5b702b17e01bb8d4625a837abdb71086113e68
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46415904"
---
# <a name="28-directive-binding"></a>2.8 지시문 바인딩

지시문의 동적으로 바인딩하는 다음 규칙을 준수 해야 합니다.

- **에 대 한**, **섹션**, **single**, **마스터**, 및 **장벽** 지시문 바인딩할를 동적으로 바깥쪽 **병렬**의 값에 관계 없이, 있는 경우 **경우** 지시문에 있을 수 있는 절. 병렬 영역 없음 현재 실행 중인 경우 지시문은 마스터 스레드만 이루어진 팀에서 실행 됩니다.

- 합니다 **정렬** 지시문에 바인딩한 동적으로 바깥쪽 **에 대 한**합니다.

- **원자성** 와 관련 하 여 배타적 액세스를 적용 하는 지시문 **원자성** 모든 스레드를 통해 현재 팀 뿐 아니라의 지시문입니다.

- **중요 한** 와 관련 하 여 배타적 액세스를 적용 하는 지시문 **중요 한** 모든 스레드를 통해 현재 팀 뿐 아니라의 지시문입니다.

- 지시문 수를 가장 가까운 바깥쪽 모든 지시문에 동적으로 바인딩하지 않도록 바깥쪽 **병렬**합니다.