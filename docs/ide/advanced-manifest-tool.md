---
title: 고급, 매니페스트 도구, 구성 속성, &lt;Projectname&gt; 속성 페이지 대화 상자
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCManifestTool.KeyFile
- VC.Project.VCManifestTool.UpdateFileHashes
- VC.Project.VCManifestTool.UpdateFileHashesSearchPath
- VC.Project.VCManifestTool.ValidateSignature
- VC.Project.VCManifestTool.KeyContainer
ms.assetid: 3d587366-05ea-4956-a978-313069660735
ms.openlocfilehash: 183b4613362acde9f48c98ee00a76b1fb8a2c4d3
ms.sourcegitcommit: dedd4c3cb28adec3793329018b9163ffddf890a4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "57742272"
---
# <a name="advanced-manifest-tool-configuration-properties-ltprojectnamegt-property-pages-dialog-box"></a>고급, 매니페스트 도구, 구성 속성, &lt;Projectname&gt; 속성 페이지 대화 상자

이 대화 상자를 사용하여 [Mt.exe](https://msdn.microsoft.com/library/aa375649)에 대한 고급 옵션을 지정합니다.

이 속성 페이지 대화 상자에 액세스하려면 프로젝트 또는 속성 시트의 속성 페이지를 엽니다. **구성 속성**에서 **매니페스트 도구** 노드를 확장한 다음, **고급**을 선택합니다.

## <a name="uielement-list"></a>UI 요소 목록

- **파일 해시 업데이트**

   /hashupdate 옵션을 사용하여 매니페스트 도구가 `<file>` 요소에 지정된 파일의 해시를 계산한 다음, 계산된 값으로 해시 특성을 업데이트하도록 지정합니다.

- **파일 해시 업데이트 검색 경로**

   `<file>` 요소에서 참조되는 파일의 검색 경로를 지정합니다. 이 옵션은 /hashupdate 옵션도 사용합니다.

## <a name="see-also"></a>참고 항목

[\<file> 요소](/visualstudio/deployment/file-element-clickonce-application)<br>
[ndptecclick](/visualstudio/deployment/clickonce-application-manifest)<br>
[매니페스트 도구 속성 페이지](../ide/manifest-tool-property-pages.md)<br>
[프로젝트 속성 사용](../ide/working-with-project-properties.md)
