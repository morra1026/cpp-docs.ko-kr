---
title: 도구 모음 단추 속성 (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- size, toolbar buttons
- toolbar buttons [C++], setting properties
- Toolbar editor [C++], toolbar button properties
- status bars [C++], active toolbar button text
- command IDs, toolbar buttons
- width, toolbar buttons
ms.assetid: b2705814-7c5d-4f24-8f77-07559b0cdda2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 02ab081446af908f2efdc06b647efcc4e76addf4
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46411510"
---
# <a name="toolbar-button-properties-c"></a>도구 모음 단추 속성 (c + +)

도구 모음 단추의 속성을 다음과 같습니다.

|속성|설명|
|--------------|-----------------|
|**ID**|단추에 대 한 ID를 정의합니다. 드롭다운 목록에는 일반적인 나와 **ID** 이름입니다.|
|**너비**|단추의 너비를 설정합니다. 16 픽셀을 사용 하는 것이 좋습니다.|
|**높이**|단추의 높이 설정합니다. 하나의 단추의 높이 도구 모음에서 모든 단추의 높이 변경 하는 참고 합니다. 15 픽셀을 사용 하는 것이 좋습니다.|
|**프롬프트**|상태 표시줄에 표시 되는 메시지를 정의 합니다. 도구 모음 단추를 도구 설명 추가 \n 및 이름을 추가 합니다. 자세한 내용은 [도구 설명을 만드는](../windows/creating-a-tool-tip-for-a-toolbar-button.md)합니다.|

**너비** 하 고 **높이** 모든 단추에 적용 합니다. 도구 모음을 만드는 데 사용 되는 비트맵은 2048의 최대 너비입니다. 따라서 단추 너비를 512로 설정 하는 경우 수만 단추 4 개 있고 513를 너비를 설정 하면 세 개의 단추만 넣을 수 있습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리 되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대 한 내용은 참조 하세요 [데스크톱 앱에 대 한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)합니다. 전역화 및 지역화 관리 되는 앱의 리소스에 대 한 내용은 참조 하세요 [Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)합니다.

## <a name="requirements"></a>요구 사항

MFC 또는 ATL

## <a name="see-also"></a>참고 항목

[도구 모음 단추의 속성 변경](../windows/changing-the-properties-of-a-toolbar-button.md)<br/>
[도구 모음 편집기](../windows/toolbar-editor.md)