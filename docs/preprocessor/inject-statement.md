---
title: inject_statement | Microsoft Docs
ms.custom: ''
ms.date: 10/18/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- inject_statement
dev_langs:
- C++
helpviewer_keywords:
- inject_statement attribute
ms.assetid: 07d6f0f4-d9fb-4e18-aa62-f235f142ff5e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 27b35c10e9e1953dc45dee1caf61d2e58c38d02d
ms.sourcegitcommit: 0164af5615389ffb1452ccc432eb55f6dc931047
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49808645"
---
# <a name="injectstatement"></a>inject_statement

**C + + 전용**

소스 텍스트로서 인수를 형식 라이브러리 헤더에 삽입합니다.

## <a name="syntax"></a>구문

```
inject_statement("source_text")
```

### <a name="parameters"></a>매개 변수

*source_text*<br/>
형식 라이브러리 헤더 파일에 삽입되는 소스 텍스트입니다.

## <a name="remarks"></a>설명

헤더 파일의 형식 라이브러리 내용을 래핑하는 네임스페이스 선언의 시작 부분에 텍스트가 배치됩니다.

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)