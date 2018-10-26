---
title: 공급자 용 프로젝트 만들기 | Microsoft Docs
ms.custom: ''
ms.date: 10/22/2018
ms.technology:
- cpp-data
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- ATL projects, creating
- OLE DB providers, projects
- projects [C++], creating
ms.assetid: 076a75de-1d4b-486a-bcf8-9c0f6b049fa2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 0f4049190ac30cfff634d4cfef82410ccfdf1314
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50063083"
---
# <a name="creating-a-project-for-the-provider"></a>공급자용 프로젝트 만들기

## <a name="to-create-a-project-in-which-the-ole-db-provider-will-reside"></a>OLE DB 공급자는 귀하가 거주 하는 프로젝트를 만들려면

1. **파일** 메뉴에서 **새로 만들기**를 클릭한 다음 **프로젝트**를 클릭합니다.

   **새 프로젝트** 대화 상자가 나타납니다.

1. 에 **프로젝트 형식** 창 클릭 합니다 **설치 됨** > **Visual c + +** > **MFC/ATL** 폴더입니다. 에 **템플릿을** 창 클릭 **ATL 프로젝트**합니다.

    > [!NOTE]
    > Visual Studio의 이전 버전에서에서 프로젝트 형식의 찾을 **설치 됨** > **템플릿** > **Visual c + +**  >  **ATL**합니다.

1. 에 **이름을** 상자, 프로젝트의 이름을 입력 한 다음 클릭 **확인**합니다.

   합니다 **ATL 프로젝트 마법사** 나타납니다.

1. 에 **ATL 프로젝트 마법사**, 선택 **동적 연결 라이브러리 (DLL)** 에 대 한 **응용 프로그램 유형을**합니다.

1. **마침**을 클릭합니다.

## <a name="see-also"></a>참고 항목

[OLE DB 공급자 만들기](../../data/oledb/creating-an-ole-db-provider.md)