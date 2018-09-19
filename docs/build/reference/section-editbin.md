---
title: -SECTION (EDITBIN) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /section
dev_langs:
- C++
helpviewer_keywords:
- -SECTION editbin option
- SECTION editbin option
- alignment characters in sections
- /SECTION editbin option
ms.assetid: 4680ab4e-c984-4251-8241-93440cad7615
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3f91d467681d5a4d5bf4eaa5f042ef44b87810b3
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45701989"
---
# <a name="section-editbin"></a>/SECTION(EDITBIN)

```
/SECTION:name[=newname][,attributes][alignment]
```

## <a name="remarks"></a>설명

섹션의 개체 파일을 컴파일하거나 링크 하는 경우 설정 된 특성을 재정의 하 여 섹션의 특성을 변경이 합니다.

콜론 ( **:** )를 지정 합니다 *이름* 섹션의 합니다. 섹션의 이름을 변경 하려면 다음과 *이름을* 등호 (=)를 사용 하 여와 *newname* 섹션입니다.

섹션의 변경 하 `attributes`, 쉼표 지정 (**,**) 다음에 하나 이상의 특성 문자입니다. 특성 부정할 느낌표 (!)를 사용 하 여 해당 문자 앞에 야 합니다. 다음 문자는 메모리 특성을 지정합니다.

|특성|설정|
|---------------|-------------|
|c|코드|
|d|무시할 수|
|e|executable|
|i|초기화 된 데이터|
|k|캐시 된 가상 메모리|
|분|링크 제거|
|o|링크 정보|
|p|가상 메모리 페이징된|
|r|read|
|s|공유|
|u|초기화 되지 않은 데이터|
|주|쓰기|

컨트롤에 *맞춤*, 문자를 지정 **는** 맞춤 크기 (바이트)를 다음과 같이 설정 하는 다음 문자 중 하나가 옵니다.

|문자|맞춤 크기 (바이트)|
|---------------|-----------------------------|
|1|1|
|2|2|
|4|4|
|8|8|
|p|16|
|t|32|
|초|64|
|x|맞춤 없음|

지정 된 `attributes` 및 *맞춤* 문자 공백이 없는 문자열입니다. 문자는 대/소문자 구분 되지 않습니다.

## <a name="see-also"></a>참고 항목

[EDITBIN 옵션](../../build/reference/editbin-options.md)