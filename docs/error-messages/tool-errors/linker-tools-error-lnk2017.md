---
title: 링커 도구 오류 LNK2017 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK2017
dev_langs:
- C++
helpviewer_keywords:
- LNK2017
ms.assetid: f7c21733-b0fb-4888-a295-9b453ba6ee77
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 80af2bb6475fc37b7feba5b29bfe9c1292740286
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46022452"
---
# <a name="linker-tools-error-lnk2017"></a>링커 도구 오류 LNK2017

'세그먼트' /largeaddressaware: no 없는 잘못 된 'symbol' 재배치

32 비트 주소를 사용 하 여 64 비트 이미지를 작성 하려고 합니다. 이렇게 하려면 다음을 수행 해야 합니다.

- 고정된 로드 주소를 사용 합니다.

- 이미지를 3GB로 제한 합니다.

- 지정할 [/largeaddressaware: no](../../build/reference/largeaddressaware-handle-large-addresses.md)합니다.