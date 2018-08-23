---
title: no_registry | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- no_registry
dev_langs:
- C++
helpviewer_keywords:
- no_registry attribute
ms.assetid: d30de4e2-551c-428c-98fd-951330d578d3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 105c2b0ee4d2648a1cc43d0baca9f30146184e78
ms.sourcegitcommit: d4c803bd3a684d7951bf88dcecf1f14af43ae411
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/10/2018
ms.locfileid: "42541292"
---
# <a name="noregistry"></a>no_registry
**no_registry** 를 사용 하 여 가져온 형식 라이브러리에 대 한 레지스트리를 검색 하지 않도록 컴파일러에 지시 `#import`합니다.  
  
## <a name="syntax"></a>구문  
  
```  
#import filename no_registry  
```  
  
### <a name="parameters"></a>매개 변수  
*filename*  
형식 라이브러리입니다.  
  
## <a name="remarks"></a>설명  
 
참조 된 형식 라이브러리가 포함 디렉터에 없는 경우 형식 라이브러리는 레지스트리에서 하는 경우에 컴파일이 실패 합니다.  **no_registry** 암시적으로 사용 하 여 가져온 다른 형식 라이브러리에 전파 `auto_search`합니다.  
  
컴파일러는 파일 이름으로 지정되고 `#import`에 직접 전달된 형식 라이브러리를 레지스트리에서 검색하지 않습니다.  
  
때 `auto_search` 지정 된 추가 `#import`사용 하 여 생성 됩니다 합니다 **no_registry** 초기 설정 `#import` (하는 경우 초기 `#import` 지시문 **no_registry** , `auto_search`-생성 `#import` 이기도 **no_registry**.)  
  
**no_registry** 레지스트리에서 파일의 이전 버전을 찾는 컴파일러의 위험 없이 참조 된 형식 라이브러리 간 가져오려는 경우에 유용 합니다. **no_registry** 형식 라이브러리 등록 되지 않은 경우에 유용한 이기도 합니다.  
  
## <a name="see-also"></a>참고 항목  
 
[#import 특성](../preprocessor/hash-import-attributes-cpp.md)   
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)