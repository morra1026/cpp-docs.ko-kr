---
title: 2.7.2.4 공유 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: c9c5d653-58fc-4620-ab0a-443ac4f8ba2e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9d1a545f1c505f9f578cad682399c8d69a882824
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46400148"
---
# <a name="2724-shared"></a>2.7.2.4 공유됨

이 절에 표시 되는 변수를 공유 합니다 *변수 목록* 팀의 모든 스레드 간에 합니다. 팀 내에서 모든 스레드는 동일한 저장소 영역에 대 한 액세스 **공유** 변수입니다.

구문의 합니다 **공유** 절은 다음과 같습니다.

```
shared(variable-list)
```