---
title: FactoryCacheFlags 열거형 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::FactoryCacheFlags
dev_langs:
- C++
ms.assetid: 6f54258f-0144-4264-9608-414e5905f6fb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 900ab21b72434c430ef65e7d6745731bbfd42002
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42593377"
---
# <a name="factorycacheflags-enumeration"></a>FactoryCacheFlags 열거형

팩터리 개체를 캐시하는지 여부를 결정합니다.

## <a name="syntax"></a>구문

```cpp
enum FactoryCacheFlags;
```

## <a name="remarks"></a>설명

기본적으로 팩터리 캐싱 정책은로 지정 합니다 [ModuleType](../windows/moduletype-enumeration.md) 만들 때 템플릿 매개 변수를 [모듈](../windows/module-class.md) 개체입니다. 이 정책을 재정의 하려면 지정 된 **FactoryCacheFlags** 팩터리 개체를 만들 때 값입니다.

|||
|-|-|
|`FactoryCacheDefault`|`Module` 개체의 캐싱 정책이 사용됩니다.|
|`FactoryCacheEnabled`|`ModuleType` 개체를 만드는 데 사용된 `Module` 템플릿 매개 변수에 관계없이 팩터리 캐싱을 사용합니다.|
|`FactoryCacheDisabled`|`ModuleType` 개체를 만드는 데 사용된 `Module` 템플릿 매개 변수에 관계없이 팩터리 캐싱을 사용하지 않습니다.|

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)