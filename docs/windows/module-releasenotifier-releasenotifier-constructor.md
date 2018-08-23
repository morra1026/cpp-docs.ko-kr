---
title: Module::ReleaseNotifier::ReleaseNotifier 생성자 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::ReleaseNotifier::ReleaseNotifier
dev_langs:
- C++
helpviewer_keywords:
- ReleaseNotifier, constructor
ms.assetid: 889a3c9a-2366-44a1-ba7d-a59c1885e7f3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f4ab2d5d03516147acda38ea2133d7445695de80
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42598790"
---
# <a name="modulereleasenotifierreleasenotifier-constructor"></a>Module::ReleaseNotifier::ReleaseNotifier 생성자

새 인스턴스를 초기화 합니다 **module:: releasenotifier** 클래스입니다.

## <a name="syntax"></a>구문

```cpp
ReleaseNotifier(bool release) throw();
```

### <a name="parameters"></a>매개 변수

*release*  
**true** 삭제 하려면이 인스턴스에 `Release` 메서드 호출 됩니다. **false** 이 인스턴스를 삭제 하지 않도록 합니다.

## <a name="exceptions"></a>예외

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Module::ReleaseNotifier 클래스](../windows/module-releasenotifier-class.md)