---
title: 2.4 작업 공유 구문
ms.date: 11/04/2016
ms.assetid: 25bb4ded-8466-4daa-a863-766b5a99b995
ms.openlocfilehash: e7bf8d37ecdc6a3ef451c9d9746fb47a76a16eb4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50502884"
---
# <a name="24-work-sharing-constructs"></a>2.4 작업 공유 구문

작업 공유 구문이 발생 하는 팀 구성원 중에서 연결된 된 문 실행을 배포 합니다. 작업 공유 지시문은 새 스레드를 시작 하지 및 작업 공유 구문에 대 한 항목에는 묵시적된 장벽이 없습니다.

작업 공유 시퀀스를 생성 하 고 **장벽** 팀의 모든 스레드에 대해 발생 하는 지시문 같아야 합니다.

OpenMP 다음 작업 공유 생성자를 정의 하 고 섹션에 설명 된 이러한:

- **에 대 한** 지시문

- **섹션** 지시문

- **단일** 지시문