---
title: 1. 소개
ms.date: 11/04/2016
ms.assetid: c42e72bc-0e31-4b1c-b670-cd82673c0c5a
ms.openlocfilehash: b365ff828fd7dc2b7d9d3136a4fbfb68c43902ce
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50554715"
---
# <a name="1-introduction"></a>1. 소개

이 문서는 컴파일러 지시문, 라이브러리 함수 및 C 및 c + + 프로그램에서 공유 메모리 병렬 처리를 지정 하는 환경 변수 컬렉션을 지정 합니다. 이 문서에서 설명한 기능 이라고 통칭 합니다 *OpenMP C/c + + 응용 프로그램 인터페이스 (API)* 합니다. 이 사양의 목적은 모델을 제공 하는 병렬 프로그래밍에 대 한 여러 공급 업체에서 공유 메모리 아키텍처 간에 이식 가능 하도록 프로그램을 허용 합니다. OpenMP C/c + + API는 다양 한 공급 업체에서는 컴파일러에서 지원 됩니다. OpenMP에 대 한 자세한 내용은 포함 하 여는 *OpenMP Fortran 응용 프로그램 인터페이스*, 다음 웹 사이트에서 확인할 수 있습니다.

[http://www.openmp.org](http://www.openmp.org)

지시문, 라이브러리 함수 및이 문서에 정의 된 환경 변수 이식성을 허용 하는 동안 병렬 프로그램을 만들고 사용자가 허용 됩니다. 지시문은 C를 확장 하 고 여러 데이터 (SPMD) 구문, 작업 공유 구문 및 동기화 구문을 프로그램 하나를 사용 하 여 c + + 순차 프로그래밍 모델 데이터의 개인화 하 고 공유 하기 위한 지원을 제공 합니다. OpenMP C 및 c + + API를 지 원하는 컴파일러 명령줄 옵션을 활성화 하 고 모든 OpenMP 컴파일러 지시문의 해석을 허용 하는 컴파일러에 포함 됩니다.