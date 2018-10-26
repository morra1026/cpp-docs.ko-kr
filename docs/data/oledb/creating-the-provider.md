---
title: 공급자 만들기 | Microsoft Docs
ms.custom: ''
ms.date: 10/15/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- OLE DB providers, creating
ms.assetid: 2506ba8f-010d-4231-aac1-387432f7b6b9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 230620a2375ac5aa822e55496d1f26751ee6f7b3
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50055348"
---
# <a name="creating-the-provider"></a>공급자 만들기

## <a name="to-create-an-ole-db-provider-with-the-atl-ole-db-provider-wizard"></a>ATL OLE DB 공급자 마법사를 사용 하 여 OLE DB 공급자를 만들려면

1. 프로젝트를 마우스 오른쪽 단추로 클릭 합니다.

1. 바로 가기 메뉴에서 클릭 **추가**를 클릭 하 고 **클래스 추가**합니다.

1. 에 **클래스 추가** 대화 상자의 **설치 됨** > **Visual c + +** > **ATL**를 선택 합니다 **ATL OLEDB 공급자** 아이콘과 클릭 **열려**합니다.

1. 에 **ATL OLE DB 공급자 마법사**, 공급자의 짧은 이름을 입력 합니다 **짧은 이름** 상자. 다음 항목의 짧은 이름을 사용 *사용자 지정*, 하지만 다른 이름을 사용할 수 있습니다. 다른 이름 입력란을 입력 하는 이름에 따라 채워집니다.

1. 필요한 경우 다른 이름 입력란을 편집 합니다. 개체 및 파일 이름 외에도 다음을 편집할 수 있습니다.

   - **Coclass**: COM 공급자를 만드는 데 사용 하는 이름입니다.

   - **ProgID**: GUID 대신 사용할 수 있는 텍스트 문자열의 프로그래밍 식별자입니다.

   - **버전**: ProgID와 Coclass 버전별 프로그래밍 방식으로 ID를 생성 하는 데 사용

1. **마침**을 클릭합니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 만들기](../../data/oledb/creating-an-ole-db-provider.md)
