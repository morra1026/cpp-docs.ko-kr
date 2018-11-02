---
title: 규칙에서 경로 검색
ms.date: 11/04/2016
helpviewer_keywords:
- search paths in NMAKE inference rules
- inference rules in NMAKE
- rules, inference
ms.assetid: 38feded6-536d-425d-bf40-fff3173a5506
ms.openlocfilehash: 26b02fa76920f0d0ff380dacd5aa76cfe8e92c79
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50649971"
---
# <a name="search-paths-in-rules"></a>규칙에서 경로 검색

```
{frompath}.fromext{topath}.toext:
   commands
```

## <a name="remarks"></a>설명

유추 규칙 종속성에 정확 하 게 지정 하는 경로가 유추 규칙 경로 일치 하는 경우에 종속성에 적용 됩니다. 종속 항목의 디렉터리 지정 *frompath* 및 대상의 디렉터리 *topath*; 공백이 허용 됩니다. 각 확장에 대 한 하나의 경로 지정 합니다. 이상의 확장 프로그램의 경로 다른 경로 필요합니다. 현재 디렉터리를 지정 하려면 마침표 (.) 또는 빈 중괄호 ({})를 사용 합니다. 매크로 나타낼 수 있습니다 *frompath* 하 고 *topath*; 전처리 중에 호출 됩니다.

## <a name="example"></a>예제

### <a name="code"></a>코드

```
{dbi\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUDBI) $<

{ilstore\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<

{misc\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{misc\}.c{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<

{msf\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<

{bsc\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{mre\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{namesrvr\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{src\cvr\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<
```

## <a name="see-also"></a>참고 항목

[규칙 정의](../build/defining-a-rule.md)