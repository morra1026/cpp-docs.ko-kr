---
title: '다중 스레딩: MFC 프로그래밍 팁 | Microsoft Docs'
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- multithreading [C++], programming tips
- handle maps [C++]
- access control [C++], multithreading
- objects [C++], multiple threads and
- non-MFC threads [C++]
- threading [MFC], programming tips
- critical sections [C++]
- synchronization [C++], multithreading
- programming [C++], multithreaded
- communications [C++], between threads
- threading [C++], best practices
- troubleshooting [C++], multithreading
- Windows handle maps [C++]
ms.assetid: ad14cc70-c91c-4c24-942f-13a75e58bf8a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3de0f200688062904a47128d9798a9ae39b652d8
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46425462"
---
# <a name="multithreading-mfc-programming-tips"></a>다중 스레딩: MFC 프로그래밍 팁

다중 스레드 응용 프로그램에는 단일 스레드 응용 프로그램 의도 된 순서에서 연산이 수행 하 고 여러 스레드에서 액세스 되는 데이터 손상 되지 보다 엄격한 주의가 필요 합니다. 이 항목에서는 Microsoft Foundation 클래스 (MFC) 라이브러리를 사용 하 여 다중 스레드 응용 프로그램을 프로그래밍 하는 경우 잠재적인 문제를 방지 하는 방법에 설명 합니다.

- [여러 스레드에서 개체에 액세스](#_core_accessing_objects_from_multiple_threads)

- [비 MFC 스레드에서 MFC 개체 액세스](#_core_accessing_mfc_objects_from_non.2d.mfc_threads)

- [Windows 핸들 맵](#_core_windows_handle_maps)

- [스레드 간 통신](#_core_communicating_between_threads)

##  <a name="_core_accessing_objects_from_multiple_threads"></a> 여러 스레드에서 개체에 액세스

단독으로 MFC 개체는 스레드로부터 안전 하지 않습니다. 두 개의 별도 스레드는 중요 섹션 같은 mfc 동기화 및/또는 적절 한 Win32 동기화 개체를 사용 하지 않는 한 동일한 개체를 조작할 수 없습니다. 임계 영역 및 기타에 대 한 자세한 내용은 관련 개체를 참조 하세요 [동기화](/windows/desktop/Sync/synchronization) Windows SDK에 있습니다.

클래스 라이브러리 디버그 메모리 할당에 의해 사용 되는 전역 데이터 구조를 보호 하기 위해 내부적으로 중요 섹션을 사용 합니다.

##  <a name="_core_accessing_mfc_objects_from_non.2d.mfc_threads"></a> 비 MFC 스레드에서 MFC 개체 액세스

스레드를 만드는 방식으로 사용 하는 다중 스레드 응용 프로그램의 경우는 [CWinThread](../mfc/reference/cwinthread-class.md) 개체를 해당 스레드에서 다른 MFC 개체를 액세스할 수 없습니다. 즉, 보조 스레드에서 MFC 개체에 액세스 하려는 경우 만들어야 스레드에 설명 된 방법 중 하나를 사용 하 여 [다중 스레딩: 사용자 인터페이스 스레드 만들기](multithreading-creating-user-interface-threads.md) 또는 [다중 스레딩: 작업자 스레드 만들기](multithreading-creating-worker-threads.md)합니다. 이러한 메서드는 다중 스레드 응용 프로그램을 처리 하는 데 필요한 내부 변수를 초기화 하는 클래스 라이브러리를 사용할 수 있는 유일한입니다.

##  <a name="_core_windows_handle_maps"></a> Windows 핸들 맵

일반적으로 스레드 만든 MFC 개체 에서만 액세스할 수 있습니다. 즉, 임시 및 영구 Windows 핸들 맵 여러 스레드에서 동시 액세스 로부터 보호를 유지 하기 위해 스레드 로컬 저장소에 보관 됩니다. 작업자 스레드 수 없습니다. 계산을 수행 하 고 다음 문서를 호출 하는 예를 들어, `UpdateAllViews` 는 창을 수정 하 여 새 데이터에는 뷰가 포함 된 멤버 함수입니다. 아무런 영향이 전혀 있으므로에서 지도 `CWnd` Hwnd 개체는 기본 스레드에서 로컬입니다. 즉, 하나의 스레드를 c + + 개체에 대 한 Windows 핸들에서 매핑이 있을 수 있지만 다른 스레드가 다른 c + + 개체에는 동일한 핸들을 매핑할 수 있습니다. 다른 스레드 하나에서 변경한 내용은 반영 되지 됩니다.

이 문제를 해결 하는 방법은 여러 가지가 있습니다. 첫 번째 작업자 스레드에 대 한 c + + 개체 대신 개별 핸들 (HWND) 등을 전달 하는 것입니다. 작업자 스레드가 추가 다음 적절 한 호출 하 여 이러한 개체를를 임시 맵에 `FromHandle` 멤버 함수입니다. 또한 개체 스레드의 영구 지도를 호출 하 여 추가할 수 있습니다 `Attach`, 하지만 개체는 스레드보다 더 이상 존재 하는지 보장 하는 경우에 수행 해야 합니다.

에 해당 하는 작업이 나와 작업자 스레드가 수행 되며 응용 프로그램의 주 창에 이러한 메시지를 게시 하는 새 사용자 정의 메시지를 만드는 또 다른 방법은 사용 하 여 `::PostMessage`입니다. 이 통신 메서드를 제외 하 고 두 스레드 모두 동일한 주소 공간에서 실행 되는 대화는 두 개의 다른 응용 프로그램와 비슷합니다.

핸들 맵에 대 한 자세한 내용은 참조 하세요. [기술 참고 3](../mfc/tn003-mapping-of-windows-handles-to-objects.md)합니다. 스레드 로컬 저장소에 대 한 자세한 내용은 참조 하세요. [스레드 로컬 저장소](/windows/desktop/ProcThread/thread-local-storage) 하 고 [스레드 로컬 저장소를 사용 하 여](/windows/desktop/ProcThread/using-thread-local-storage) Windows SDK에 있습니다.

##  <a name="_core_communicating_between_threads"></a> 스레드 간 통신

MFC에는 여러 스레드 보안을 유지 하는 개체에 대 한 액세스를 동기화 하는 스레드를 허용 하는 클래스를 제공 합니다. 이러한 클래스의 사용에 설명 되어 [다중 스레딩: 동기화 클래스 사용 방법](multithreading-how-to-use-the-synchronization-classes.md) 하 고 [다중 스레딩: 동기화 클래스를 사용 하는 경우](multithreading-when-to-use-the-synchronization-classes.md)합니다. 이러한 개체에 대 한 자세한 내용은 참조 하세요. [동기화](/windows/desktop/Sync/synchronization) Windows SDK에 있습니다.

## <a name="see-also"></a>참고 항목

[C++ 및 MFC에서 다중 스레딩](multithreading-with-cpp-and-mfc.md)