---
title: '방법: 등록이 필요 없는 COM 구성 요소 빌드'
ms.date: 11/04/2016
helpviewer_keywords:
- COM components, registration-free
ms.assetid: 7e585d6a-0314-45b2-8f1b-cae9ac4df037
ms.openlocfilehash: 4f4ebf121b761c37969fa3f9788bda52d913f340
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50463533"
---
# <a name="how-to-build-registration-free-com-components"></a>방법: 등록이 필요 없는 COM 구성 요소 빌드

등록이 필요 없는 COM 구성 요소 매니페스트를 Dll에 기본 제공 되는 COM 구성 요소 이며

### <a name="to-build-manifests-into-com-components"></a>COM 구성 요소에 매니페스트를 빌드

1. COM 구성 요소에 대 한 프로젝트 속성 페이지를 엽니다.

1. 확장을 **구성 속성** 노드를 차례로 확장 합니다 **매니페스트 도구** 노드.

1. 선택 된 **입력 및 출력** 속성 페이지 및 설정 합니다 **매니페스트 포함** 속성이 **예**합니다.

1. **확인**을 클릭합니다.

1. 솔루션을 빌드합니다.

## <a name="see-also"></a>참고 항목

[격리된 응용 프로그램](/windows/desktop/SbsCs/isolated-applications)<br/>
[Side-by-side-어셈블리에 대 한](/windows/desktop/SbsCs/about-side-by-side-assemblies-)<br/>
[방법: COM 구성 요소를 사용하는 격리된 응용 프로그램 빌드](../build/how-to-build-isolated-applications-to-consume-com-components.md)