---
title: marshal_context 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- marshal_context
dev_langs:
- C++
helpviewer_keywords:
- marshal_context class [C++]
ms.assetid: 241b0cf6-4ca4-4812-aaee-d671c11dc034
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: fc3399ee088a0430ca857c3e421742ee484d337a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46413318"
---
# <a name="marshalcontext-class"></a>marshal_context 클래스

이 클래스는 네이티브 및 관리 되는 환경 간에 데이터를 변환합니다.

## <a name="syntax"></a>구문

```
class marshal_context
```

## <a name="remarks"></a>설명

사용 된 `marshal_context` 컨텍스트를 필요로 하는 데이터 변환에 대 한 클래스입니다. 참조 [Overview of Marshaling c + +에서](../dotnet/overview-of-marshaling-in-cpp.md) 는 변환이 필요한 컨텍스트 및 마샬링 파일에 포함 되도록 하는 방법에 대 한 자세한 내용은 합니다. 마샬링 컨텍스트를 사용 하는 경우의 결과 까지만 유효 합니다 `marshal_context` 개체는 소멸 됩니다. 결과 유지 하려면 데이터를 복사 해야 합니다.

동일한 `marshal_context` 여러 개의 데이터 변환을 사용할 수 있습니다. 이 방식으로 컨텍스트를 다시 사용 마샬링 이전 호출의 결과 결과는 영향이 없습니다.

## <a name="requirements"></a>요구 사항

**헤더 파일:** \<msclr\marshal.h >, \<msclr\marshal_windows.h >, \<msclr\marshal_cppstd.h >, 또는 \<msclr\marshal_atl.h >

**Namespace:** msclr::interop

## <a name="see-also"></a>참고 항목

[C++ 마샬링 개요](../dotnet/overview-of-marshaling-in-cpp.md)<br/>
[marshal_as](../dotnet/marshal-as.md)