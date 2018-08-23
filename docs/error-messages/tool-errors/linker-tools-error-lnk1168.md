---
title: 링커 도구 오류 LNK1168 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1168
dev_langs:
- C++
helpviewer_keywords:
- LNK1168
ms.assetid: 97ead151-fd99-46fe-9a1d-7e84dc0b8cc8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9437b88b67254a63babf5b72379a760d1ab86062
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42541866"
---
# <a name="linker-tools-error-lnk1168"></a>링커 도구 오류 LNK1168
filename을(를) 쓰기용으로 열 수 없습니다.  
  
 링커는 `filename`에 쓸 수 없습니다. 파일이 사용 중이고 파일 핸들이 다른 프로세스에 의해 잠겨 있거나, 파일 또는 파일이 있는 디렉터리나 네트워크 공유에 대한 쓰기 권한이 없을 수 있습니다. 이 오류는 일시적인 조건으로 자주 발생 — 예 바이러스 백신 프로그램이 보유 한 잠금 파일 검색 인덱싱 프로세스 또는 Visual Studio 빌드 시스템에서 잠금 해제 지연 보유 합니다.  
  
 이 문제를 해결하려면 `filename` 파일 핸들이 잠겨 있지 않은지, 파일에 대해 쓰기 권한이 있는지 확인합니다. 실행 파일이라면 이미 실행 중이 아닌지 확인합니다.  
  
 Windows SysInternals 유틸리티를 사용할 수 있습니다 [처리할](http://technet.microsoft.com/sysinternals/bb896655.aspx) 또는 [Process Explorer](http://technet.microsoft.com/sysinternals/bb896653) 프로세스에 파일 핸들 잠금이에서 확인 하려면 `filename`합니다. 프로세스 탐색기를 사용하여 열린 파일 핸들에 대한 잠금을 해제할 수도 있습니다. 이러한 유틸리티를 사용하는 방법에 대한 자세한 내용은 함께 제공된 도움말 파일을 참조하세요.  
  
 파일이 바이러스 백신 프로그램으로 잠겨 있으면 백신 프로그램의 자동 검색에서 빌드 출력 디렉터리를 제외하여 이 문제를 해결할 수 있습니다. 바이러스 검색 프로그램은 종종 파일 시스템에서 새 파일 생성에 의해 트리거되며 검색이 진행되는 동안 파일에 대해 잠금을 설정합니다. 검색에서 특정 디렉터리를 제외하는 방법에 대한 자세한 내용은 바이러스 백신 프로그램 설명서를 참조하세요.  
  
 파일이 검색 인덱싱 서비스에 의해 잠겨 있으면 자동 인덱싱에서 빌드 출력 디렉터리를 제외하여 이 문제를 해결할 수 있습니다. 자세한 내용은 인덱싱 서비스의 설명서를 참조하세요. Windows 검색 인덱싱 서비스를 변경 하려면 사용 하 여 **인덱싱 옵션** 는 Windows에서 **제어판**합니다. 자세한 내용은 [인덱스를 사용 하 여 개선 하는 Windows 검색: 질문과 대답](http://windows.microsoft.com/en-us/windows/improve-windows-searches-using-index-faq#1TC=windows-7)합니다.  
  
 실행 파일을 빌드 프로세스에 의해 덮어쓸 수 없는 경우 파일 탐색기에 의해 잠겨 있을 수 있습니다. 경우는 **응용 프로그램 환경을** 서비스가 비활성화 되었습니다, 파일 탐색기는 실행 파일 핸들 잠금 오랜된 시간 동안 보유할 수 있습니다. 이 문제를 해결 하려면 실행 **services.msc** 연 다음 합니다 **속성** 대화 상자를 **응용 프로그램 환경을** 서비스입니다. 변경 된 **시작 유형** 에서 **사용 안 함** 에 **수동**합니다.  
  
## <a name="see-also"></a>참고 항목  
 [솔루션 또는 Visual c + +에서 ActiveX 프로젝트를 빌드하려고 할 때 "오류 PRJ0008" 또는 "심각한 오류 LNK1168" 오류 메시지가 나타날 수 있습니다.](http://support.microsoft.com/kb/308358)