---
title: 'Module:: releasenotifier:: Invoke 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::ReleaseNotifier::Invoke
dev_langs:
- C++
helpviewer_keywords:
- Invoke method
ms.assetid: f62686fe-74bf-482b-a46b-6a3c09b80e7e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: da71ab887145f3bcb1341b5ea6004a24253a4a5f
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42594502"
---
# <a name="modulereleasenotifierinvoke-method"></a>Module::ReleaseNotifier::Invoke 메서드

구현될 때 모듈의 마지막 개체가 해제되면 이벤트 처리기를 호출합니다.

## <a name="syntax"></a>구문

```cpp
virtual void Invoke() = 0;
```

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Module::ReleaseNotifier 클래스](../windows/module-releasenotifier-class.md)