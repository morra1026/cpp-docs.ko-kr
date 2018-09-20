---
title: 속성 인덱스 선언 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- indexers
- default indexers
- defaults, indexers
- indexed properties, C++
ms.assetid: d898fdbc-2106-4b6a-8c5c-9f511d80fc2f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: a6917742b285b3700548b54fef164d01c0594e5e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46380467"
---
# <a name="property-index-declaration"></a>속성 인덱스 선언

인덱싱된 속성 선언 구문이 Visual c + + Managed Extensions for c + + 변경 되었습니다.

Managed Extensions 언어 지원 인덱싱된 속성의 두 가지 주요 단점은 첨자가 클래스 수준; 제공 된 즉, 모든 인덱싱된 속성에 이름을 지정 하는 데 필요한 있고 따라서 관계가 없으므로, 예를 들어에 직접 적용할 수 있는 관리 되는 아래 첨자 연산자를 제공 하는 `Vector` 또는 `Matrix` 클래스 개체입니다. 덜 중요 한 단점은 두 번째는 인덱싱된 속성에서 속성을 구분 하기 위해 시각적으로 어렵습니다 매개 변수의 수만 표시 됩니다. 마지막으로 인덱싱되지 않은 속성의 경우와 같은 문제에서 인덱싱된 속성 저하-접근자는 원자 단위로 처리 하지 되지만 개별 메서드로 분리 합니다.  예를 들어:

```
public __gc class Vector;
public __gc class Matrix {
   float mat[,];

public:
   __property void set_Item( int r, int c, float value);
   __property float get_Item( int r, int c );

   __property void set_Row( int r, Vector* value );
   __property Vector* get_Row( int r );
};
```

추가 매개 변수를 지정 하는 두 또는 단일에 의해서만 구분 되며 여기에서 볼 수 차원 인덱스입니다. 새 구문에서 인덱서는 인덱서의 이름을 하 고 각 인덱스의 종류와 수를 나타내는 대괄호 ([,])에 의해 구별 됩니다.

```
public ref class Vector {};
public ref class Matrix {
private:
   array<float, 2>^ mat;

public:
   property float Item [int,int] {
      float get( int r, int c );
      void set( int r, int c, float value );
   }

   property Vector^ Row [int] {
      Vector^ get( int r );
      void set( int r, Vector^ value );
   }
};
```

새 구문에서 클래스의 개체에 직접 적용할 수 있는 클래스 수준 인덱서를 나타내기 위해는 `default` 키워드를 다시 사용 하는 명시적 이름으로 대체 합니다. 예를 들어:

```
public ref class Matrix {
private:
   array<float, 2>^ mat;

public:
   // ok: class level indexer now
   //
   //     Matrix mat;
   //     mat[ 0, 0 ] = 1;
   //
   // invokes the set accessor of the default indexer

   property float default [int,int] {
      float get( int r, int c );
      void set( int r, int c, float value );
   }

   property Vector^ Row [int] {
      Vector^ get( int r );
      void set( int r, Vector^ value );
   }
};
```

새 구문에서 기본 인덱싱된 속성이 지정 되 면 두 다음 이름은 예약 되어 있습니다: `get_Item` 고 `set_Item`입니다. 다음은 기본 인덱싱된 속성에 대해 생성 된 기본 이름을 때문입니다.

단순 속성 구문을 비슷합니다 단순 인덱스 구문 없음는 참고 합니다.

## <a name="see-also"></a>참고 항목

[클래스 또는 인터페이스 내에서 멤버 선언(C++/CLI)](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md)
