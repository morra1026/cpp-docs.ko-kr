---
title: ATL OLE DB 공급자 마법사 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- vc.codewiz.class.atl.provider.overview
dev_langs:
- C++
helpviewer_keywords:
- ATL OLE DB Provider Wizard
- ATL projects, adding ATL OLE DB providers
ms.assetid: cf91ba78-01d1-4d12-b673-e95d96bfbebe
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: a4bb77489a610d9331378e523b6983dcf14d996c
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43762981"
---
# <a name="atl-ole-db-provider-wizard"></a>ATL OLE DB 공급자 마법사

이 마법사에서는 OLE DB 공급자를 구성 하는 클래스를 만듭니다.

## <a name="remarks"></a>설명

Visual Studio 2008부터,이 마법사에서 생성 된 등록 스크립트 등록에서 COM 구성 요소 **HKEY_CURRENT_USER** of **HKEY_LOCAL_MACHINE**합니다. 이 동작을 수정 하려면 설정 합니다 **모든 사용자에 대 한 구성 요소 등록** ATL 마법사의 옵션입니다.

다음 표에서 ATL OLE DB 공급자 마법사에 대 한 옵션을 보여 줍니다.

**짧은 이름**  
만들어질 공급자의 짧은 이름을 입력 합니다. 다른 입력란 마법사에서 자동으로 채워집니다. 입력에 기반 합니다. 원하는 경우 다른 이름 상자를 편집할 수 있습니다.

**Coclass**  
Coclass의 이름입니다. 이 이름과 일치 하도록 ProgID 이름이 변경 됩니다.

**특성 사용**  
이 옵션은 특성 또는 템플릿 선언을 사용 하 여 공급자 클래스를 만들 여부를 지정 합니다. 이 옵션을 선택 하면 마법사 (이것이 기본 옵션 특성 사용된 프로젝트를 만든 경우) 템플릿 선언 대신 특성을 사용 합니다. 이 옵션의 선택을 취소 하면 마법사 (이것이 기본 옵션 특성을 사용 되지 않은 프로젝트를 만든 경우) 하는 특성 대신 템플릿 선언을 사용 합니다.

비-특성 프로젝트를 만들 때이 옵션을 선택 하면 프로젝트 특성 사용된 프로젝트를 변환할을 계속할지 여부를 묻는 마법사 경고 합니다.

**ProgID**  
ProgID 또는 프로그래밍 방식 식별자는 응용 프로그램 GUID 대신 사용할 수 있는 텍스트 문자열. ProgID 이름은 *Projectname.Coclassname*합니다.

**Version**  
공급자의 버전 번호입니다. 기본값은 1입니다.

**DataSource 클래스**  
C 형식의 데이터 소스 클래스의 이름을*Shortname*원본입니다.

**데이터 소스.h 파일**  
데이터 소스 클래스에 대 한 헤더 파일입니다. 이 파일의이 이름을 편집 하거나 기존 헤더 파일을 선택할 수 있습니다.

**세션 클래스**  
C 형식의 세션 클래스의 이름을*Shortname*세션입니다.

**세션.h 파일**  
세션 클래스에 대 한 헤더 파일입니다. 이 파일의이 이름을 편집 하거나 기존 헤더 파일을 선택할 수 있습니다.

**명령 클래스**  
C 형식의 명령 클래스의 이름을*Shortname*명령입니다.

**명령.h 파일**  
명령 클래스에 대 한 헤더 파일입니다. 이 이름은 편집할 수 없습니다 하 고 행 집합 헤더 파일의 이름에 따라 달라 집니다.

**행 집합 클래스**  
C 형식의 행 집합 클래스의 이름을*Shortname*행 집합입니다.

**행 집합.h 파일**  
행 집합 클래스에 대 한 헤더 파일입니다. 이 파일의이 이름을 편집 하거나 기존 헤더 파일을 선택할 수 있습니다.

**행 집합.cpp 파일**  
공급자의 구현 파일입니다. 이 파일의이 이름을 편집 하거나 기존 구현 파일을 선택할 수 있습니다.

## <a name="see-also"></a>참고 항목

[ATL OLE DB 공급자](../../atl/reference/adding-an-atl-ole-db-provider.md)

