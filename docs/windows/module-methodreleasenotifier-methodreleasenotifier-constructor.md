---
title: Module::MethodReleaseNotifier::MethodReleaseNotifier 생성자 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::MethodReleaseNotifier::MethodReleaseNotifier
dev_langs:
- C++
helpviewer_keywords:
- MethodReleaseNotifier, constructor
ms.assetid: 762e2ca4-0a92-49de-9ff5-d3efa0f067c0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 608a885eb446860cca43e5fabd19597d7611e633
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46386824"
---
# <a name="modulemethodreleasenotifiermethodreleasenotifier-constructor"></a>Module::MethodReleaseNotifier::MethodReleaseNotifier 생성자

새 인스턴스를 초기화 합니다 **module:: methodreleasenotifier** 클래스입니다.

## <a name="syntax"></a>구문

```cpp
MethodReleaseNotifier(
   _In_ T* object,
   _In_ void (T::* method)(),
   bool release) throw() :
            ReleaseNotifier(release), object_(object),
            method_(method);
```

### <a name="parameters"></a>매개 변수

*object*<br/>
개체 멤버 함수가 이벤트 처리기입니다.

*method*<br/>
멤버 함수 매개 변수의 *개체* 이벤트 처리기입니다.

*release*<br/>
지정할 **true** 내부 호출을 사용 하도록 설정 하려면 [모듈:: ReleaseNotifier::Release()](../windows/module-releasenotifier-release.md) 메서드를 지정이 고, 그렇지 **false**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Module::MethodReleaseNotifier 클래스](../windows/module-methodreleasenotifier-class.md)