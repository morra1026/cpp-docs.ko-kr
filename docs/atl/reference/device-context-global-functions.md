---
title: 장치 컨텍스트 전역 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- atlwin/ATL::AtlCreateTargetDC
dev_langs:
- C++
ms.assetid: 08ec28f6-daff-4882-9544-e8a4639d05c4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 8944ecdb4f9996800264986a7a687df6020b0591
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43209935"
---
# <a name="device-context-global-functions"></a>장치 컨텍스트 전역 함수
이 함수는 지정된 된 장치에 대 한 장치 컨텍스트를 만듭니다.  
  
|||  
|-|-|  
|[AtlCreateTargetDC](#atlcreatetargetdc)|장치 컨텍스트를 만듭니다.|  
  
##  <a name="atlcreatetargetdc"></a>  AtlCreateTargetDC  
 에 지정 된 장치에 대 한 장치 컨텍스트를 만듭니다.는 [DVTARGETDEVICE](/windows/desktop/api/objidl/ns-objidl-tagdvtargetdevice) 구조입니다.  
  
```
HDC AtlCreateTargetDC(HDC hdc, DVTARGETDEVICE* ptd);
```  
  
### <a name="parameters"></a>매개 변수  
 *hdc*  
 [in] 장치 컨텍스트 또는 NULL의 기존 핸들입니다.  
  
 *ptd*  
 [in] 에 대 한 포인터를 `DVTARGETDEVICE` 대상 장치에 대 한 정보를 포함 하는 구조입니다.  
  
### <a name="return-value"></a>반환 값  
 장치 컨텍스트에 지정 된 장치에 대 한 핸들을 반환 합니다 `DVTARGETDEVICE`합니다. 장치는 지정 하는 경우 기본 디스플레이 장치에 핸들을 반환 합니다.  
  
### <a name="remarks"></a>설명  
 구조에는 NULL이 고 *hdc* NULL 이면 기본 디스플레이 장치에 대 한 장치 컨텍스트를 만듭니다.  
  
 하는 경우 *hdc* NULL이 아닌 및 *데* 가 null 인 경우 기존 반환 *hdc*합니다.  

## <a name="requirements"></a>요구 사항  
 **헤더:** atlwin.h  
   
## <a name="see-also"></a>참고 항목  
 [함수](../../atl/reference/atl-functions.md)
