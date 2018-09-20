---
title: CD2DEllipse 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- CD2DEllipse
- AFXRENDERTARGET/CD2DEllipse
- AFXRENDERTARGET/CD2DEllipse::CD2DEllipse
dev_langs:
- C++
helpviewer_keywords:
- CD2DEllipse [MFC], CD2DEllipse
ms.assetid: e9f02f54-acf2-427e-b349-db50cd9a77df
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 6acec41bcae08f5585eb521dc90ff12d082fd5ad
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46418686"
---
# <a name="cd2dellipse-class"></a>CD2DEllipse 클래스

`D2D1_ELLIPSE`의 래퍼입니다.

## <a name="syntax"></a>구문

```
class CD2DEllipse : public D2D1_ELLIPSE;
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|[CD2DEllipse::CD2DEllipse](#cd2dellipse)|오버로드됨. 생성 된 `CD2DEllipse` 에서 개체 `D2D1_ELLIPSE` 개체입니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`D2D1_ELLIPSE`

`CD2DEllipse`

## <a name="requirements"></a>요구 사항

**헤더:** afxrendertarget.h

##  <a name="cd2dellipse"></a>  CD2DEllipse::CD2DEllipse

CD2DRectF 개체에서 CD2DEllipse 개체를 생성합니다.

```
CD2DEllipse(const CD2DRectF& rect);
CD2DEllipse(const D2D1_ELLIPSE& ellipse);
  CD2DEllipse(const D2D1_ELLIPSE* ellipse);


CD2DEllipse(
    const CD2DPointF& ptCenter,
    const CD2DSizeF& sizeRadius);
```

### <a name="parameters"></a>매개 변수

*rect*<br/>
소스 사각형

*타원*<br/>
원본 타원

*ptCenter*<br/>
타원의 중심점입니다.

*sizeRadius*<br/>
X 반지름 및 Y 반경을 타원의 합니다.

## <a name="see-also"></a>참고 항목

[클래스](../../mfc/reference/mfc-classes.md)
