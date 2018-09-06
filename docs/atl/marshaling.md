---
title: 마샬링 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- marshaling, COM interop
- marshaling
- COM interfaces, marshaling
ms.assetid: 40644b0a-1106-4fc8-9dfb-9bee9915d825
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2f9e8e080837ed109a786c2123ab90624d994cd1
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43753735"
---
# <a name="marshaling"></a>마샬링

마샬링 중 COM 기술은 다른 프로세스에 사용할 하나의 프로세스에서 개체에 의해 노출 되는 인터페이스를 허용 합니다. 마샬링 COM 코드를 제공 (또는 인터페이스 구현 자가 제공한 코드를 사용 하 여)에서 프로세스 간 (물론, 다른 컴퓨터에서 실행 중인 프로세스를 통해) 이동할 수 있는 형식으로 메서드의 매개 변수 팩과 해당 매개 변수를 압축 풀기 다른 쪽 끝입니다. 마찬가지로, COM 호출에서 반환 된 값에도 이와 동일한 단계를 수행 해야 합니다.

> [!NOTE]
>  마샬링 일반적으로 필요 없는 개체와 동일한 프로세스에서 개체에서 제공 하는 인터페이스를 사용 하는 경우입니다. 그러나 마샬링 스레드 간에 필요할 수 있습니다.

## <a name="see-also"></a>참고 항목

[COM 소개](../atl/introduction-to-com.md)   
[마샬링 정보](/windows/desktop/com/marshaling-details)

