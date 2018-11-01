---
title: A.16   Locks 사용
ms.date: 11/04/2016
ms.assetid: 873bf32b-6cfe-4ce1-b994-bef80b50f399
ms.openlocfilehash: 6afb94660acdc79ea5a7eb61d3bf7e21fd70d751
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50458984"
---
# <a name="a16---using-locks"></a>A.16   Locks 사용

다음 예에서 (에 대 한 [섹션 3.2](../../parallel/openmp/3-2-lock-functions.md) 41 페이지) lock 함수 인수 형식에 있어야 하는 참고 `omp_lock_t`를 하 고 있는 플러시 필요가 없습니다.  Lock 함수 인해 스레드가 첫 번째 중요 한 섹션에서 항목을 기다리는 동안 유휴 상태 여야 하지만 두 번째 항목을 기다리는 동안 다른 작업을 수행 합니다.  `omp_set_lock` 함수 블록 이지만 `omp_test_lock` 함수 수행 skip ()에서 작업을 허용 하지 않습니다.

## <a name="example"></a>예제

### <a name="code"></a>코드

```
// omp_using_locks.c
// compile with: /openmp /c
#include <stdio.h>
#include <omp.h>

void work(int);
void skip(int);

int main() {
   omp_lock_t lck;
   int id;

   omp_init_lock(&lck);
   #pragma omp parallel shared(lck) private(id)
   {
      id = omp_get_thread_num();

      omp_set_lock(&lck);
      printf_s("My thread id is %d.\n", id);

      // only one thread at a time can execute this printf
      omp_unset_lock(&lck);

      while (! omp_test_lock(&lck)) {
         skip(id);   // we do not yet have the lock,
                     // so we must do something else
      }
      work(id);     // we now have the lock
                    // and can do the work
      omp_unset_lock(&lck);
   }
   omp_destroy_lock(&lck);
}
```