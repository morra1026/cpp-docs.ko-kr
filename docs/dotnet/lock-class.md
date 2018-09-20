---
title: lock 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- msclr::lock
- msclr.lock
- lock
dev_langs:
- C++
helpviewer_keywords:
- lock class
ms.assetid: 5123edd9-6aed-497d-9a0b-f4b6d6c0d666
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 7ef0887ca3eec7510717aab21ba4c6c7aba98d25
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46380297"
---
# <a name="lock-class"></a>lock 클래스

이 클래스는 여러 스레드에서 개체에 대 한 액세스를 동기화 하는 것에 대 한 잠금을 자동화 합니다.  생성 될 때 잠금을 획득 릴리스를 제거 하는 경우 및 잠금.

## <a name="syntax"></a>구문

```
ref class lock;
```

## <a name="remarks"></a>설명

`lock` CLR 개체에 대해서만 사용할 수 있고 CLR 코드에만 사용할 수 있습니다.

잠금 클래스는 내부적으로 <xref:System.Threading.Monitor> 액세스를 동기화 합니다. 동기화에 자세한 내용은이 항목을 참조 하세요.

## <a name="requirements"></a>요구 사항

**헤더 파일** \<msclr\lock.h >

**Namespace** msclr

## <a name="see-also"></a>참고 항목

[lock](../dotnet/lock.md)<br/>
[lock 멤버](../dotnet/lock-members.md)