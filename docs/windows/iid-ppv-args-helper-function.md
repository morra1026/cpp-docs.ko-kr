---
title: IID_PPV_ARGS_Helper 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/IID_PPV_ARGS_Helper
dev_langs:
- C++
helpviewer_keywords:
- IID_PPV_ARGS_Helper function
ms.assetid: afee9b23-8df1-4575-903f-e9ba748418f0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: a6131cea7a7684036fd7183a79214c7c6936540b
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43218750"
---
# <a name="iidppvargshelper-function"></a>IID_PPV_ARGS_Helper 함수

지정 된 인수의 형식에서 파생 되는 확인 된 `IUnknown` 인터페이스입니다.

> [!IMPORTANT]
> 이 템플릿 특수화 WRL 인프라를 지원 하며 코드에서 직접 사용할 수 없습니다. 사용 하 여 [IID_PPV_ARGS](https://msdn.microsoft.com/library/windows/desktop/ee330727.aspx) 대신 합니다.

## <a name="syntax"></a>구문

```cpp
template<typename T>
void** IID_PPV_ARGS_Helper(
   _Inout_ Microsoft::WRL::Details::ComPtrRef<T> pp
);
```

### <a name="parameters"></a>매개 변수

*T*  
인수의 형식은 *pp*합니다.

*pp*  
이중 간접 포인터입니다.

## <a name="return-value"></a>반환 값

인수 *pp* 에 대 한 포인터-에-a-포인터로 캐스팅 **void**합니다.

## <a name="remarks"></a>설명

컴파일 타임 오류가 생성 됩니다 템플릿 매개 변수 *T* 에서 파생 되지 `IUnknown`합니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

## <a name="see-also"></a>참고 항목

[참조 (Windows 런타임 라이브러리)](https://msdn.microsoft.com/00000000-0000-0000-0000-000000000000)