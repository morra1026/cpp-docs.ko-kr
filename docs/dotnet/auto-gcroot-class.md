---
title: auto_gcroot 클래스
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- msclr::auto_gcroot
- msclr.auto_gcroot
- auto_gcroot
helpviewer_keywords:
- auto_gcroot
ms.assetid: b5790912-265d-463e-a486-47302e91042a
ms.openlocfilehash: cb89035d928b251c9cc0427612ce6853a96456a9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50534240"
---
# <a name="autogcroot-class"></a>auto_gcroot 클래스

자동 리소스 관리 (같은 [auto_ptr 클래스](../standard-library/auto-ptr-class.md))는 네이티브 형식에 가상 핸들을 포함 시킬 수 있습니다.

## <a name="syntax"></a>구문

```cpp
template<typename _element_type>
class auto_gcroot;
```

#### <a name="parameters"></a>매개 변수

*_element_type*<br/>
포함할 관리 되는 형식입니다.

## <a name="requirements"></a>요구 사항

**헤더 파일** \<msclr\auto_gcroot.h >

**Namespace** msclr

## <a name="see-also"></a>참고 항목

[auto_gcroot](../dotnet/auto-gcroot.md)<br/>
[auto_gcroot 멤버](../dotnet/auto-gcroot-members.md)<br/>
[방법: 네이티브 형식으로 핸들 선언](../dotnet/how-to-declare-handles-in-native-types.md)<br/>
[auto_handle 클래스](../dotnet/auto-handle-class.md)