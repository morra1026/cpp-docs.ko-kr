---
title: C + + 언어 참조 | Microsoft Docs
ms.custom: index-page
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- language reference
- C++, language reference
- language reference, Visual C++
- Visual C++, language reference
ms.assetid: 4be9cacb-c862-4391-894a-3a118c9c93ce
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 708db2b20cdbbe2e322075789f64433ff70612a2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46025518"
---
# <a name="c-language-reference"></a>C++ 언어 참조

이 참조는 Microsoft Visual C++에서 구현되는 것처럼 C++ 프로그래밍 언어를 설명합니다. 기반으로 *The Annotated c + + Reference Manual* 구성은 Margaret Ellis와 Bjarne Stroustrup 및 ANSI/ISO c + + 국제 표준 (ISO/IEC FDIS 14882). C++ 언어 기능의 Microsoft 전용 구현이 포함되어 있습니다.

최신 c + + 프로그래밍 방법의 개요를 참조 하세요 [진화 c + +](welcome-back-to-cpp-modern-cpp.md)합니다.

키워드 또는 연산자를 빠르게 찾으려면 다음 표를 참조하십시오.

- [C + + 키워드](../cpp/keywords-cpp.md)

- [C++ 연산자](../cpp/cpp-built-in-operators-precedence-and-associativity.md)

## <a name="in-this-section"></a>섹션 내용

[어휘 규칙](../cpp/lexical-conventions.md) c + + 프로그램의 기본적인 어휘 요소: 토큰, 주석, 연산자, 키워드, 문장 부호, 리터럴이 있습니다. 또한 파일 변환, 연산자 우선 순위/결합성이 있습니다.

[기본 개념](../cpp/basic-concepts-cpp.md) 범위, 링크, 프로그램 시작 및 종료, 저장소 클래스 및 형식입니다.

[표준 변환](../cpp/standard-conversions.md) 기본 제공 또는 "기본" 형식 사이의 형식 변환 합니다. 또한 산술 변환 및 포인터, 참조 및 멤버 포인터 형식 간의 변환입니다.

[연산자, 우선 순위 및 결합성](../cpp/cpp-built-in-operators-precedence-and-associativity.md) c + +의 연산자입니다.

[식](../cpp/expressions-cpp.md) 유형의 식에 식의 의미 체계 연산자, 캐스팅 및 캐스팅 연산자, 런타임 형식 정보에 대 한 항목을 참조 합니다.

[람다 식](../cpp/lambda-expressions-in-cpp.md) 암시적으로 함수 개체 클래스를 정의 하 고 해당 클래스 형식의 함수 개체를 생성 하는 프로그래밍 기법입니다.

[문을](../cpp/statements-cpp.md) 식, null, 복합, 선택, 반복, 점프 및 선언 문의 합니다.

[선언 및 정의](declarations-and-definitions-cpp.md) 저장소 클래스 지정자, 함수 정의 초기화, 열거형 **클래스**하십시오 **구조체**, 및 **union** 선언 및 **typedef** 선언 합니다. 또한 **인라인** 함수 **const** 키워드, 네임 스페이스입니다.

[클래스, 구조체 및 공용 구조체](../cpp/classes-and-structs-cpp.md) 클래스, 구조체 및 공용 구조체를 소개 합니다. 또한 멤버 함수, 특수 멤버 함수, 데이터 멤버, 비트 필드를 **이** 포인터, 중첩된 클래스입니다.

[파생 클래스](../cpp/inheritance-cpp.md) 단일 및 다중 상속 **가상** 함수, 다중 기본 클래스 **추상** 클래스 범위 규칙입니다. 또한 합니다 **__super** 하 고 **__interface** 키워드입니다.

[멤버 Access Control](../cpp/member-access-control-cpp.md) 클래스 멤버에 대 한 액세스 제어: **공용**, **사설**, 및 **보호** 키워드입니다. Friend 함수 및 클래스입니다.

[오버 로드](operator-overloading.md) 오버 로드 된 연산자, 연산자 오버 로드에 대 한 규칙입니다.

[예외 처리](../cpp/exception-handling-in-visual-cpp.md) c + + 예외 처리, 구조적된 예외 처리 (SEH) 예외 처리 문을 작성에 사용 된 키워드입니다.

[어설션 및 User-Supplied 메시지](../cpp/assertion-and-user-supplied-messages-cpp.md) 
 `#error` 지시문을 **static_assert** 키워드는 `assert` 매크로입니다.

[템플릿을](../cpp/templates-cpp.md) 템플릿 지정, 함수 템플릿, 클래스 템플릿 **typename** 키워드, 템플릿 및 매크로, 템플릿 및 스마트 포인터입니다.

[이벤트 처리](../cpp/event-handling.md) 이벤트 및 이벤트 처리기를 선언 합니다.

[Microsoft 전용 한정자](../cpp/microsoft-specific-modifiers.md) Microsoft c + + 전용 한정자. 메모리 주소 지정, 호출 규칙을 **naked** 함수를 확장 저장소 클래스 특성 (**__declspec**), **__w64**합니다.

[인라인 어셈블러](../assembler/inline/inline-assembler.md) 어셈블리 언어 및 c + +에서 사용 하 여 **__asm** 블록입니다.

[컴파일러 COM 지원](../cpp/compiler-com-support.md) Microsoft 전용 클래스 및 COM 형식을 지 원하는 데 사용 되는 전역 함수에 대 한 참조입니다.

[Microsoft 확장](../cpp/microsoft-extensions.md) c + +에 대 한 Microsoft 확장입니다.

[비표준 동작](../cpp/nonstandard-behavior.md) Visual c + + 컴파일러의 비표준 동작에 대 한 정보입니다.

[C + +를 다시 시작](welcome-back-to-cpp-modern-cpp.md) 안전 하 고, 올바른 효율적인 프로그램을 작성 하는 것에 대 한 최신 c + + 프로그래밍 개요 사례입니다.

## <a name="related-sections"></a>관련 단원

[런타임 플랫폼용 구성 요소 확장명](../windows/component-extensions-for-runtime-platforms.md) Visual c + +를 사용 하 여 공용 언어 런타임을 대상에 대 한 자료를 참조 합니다.

[C/c + + 빌드 참조](../build/reference/c-cpp-building-reference.md) 컴파일러 옵션, 링커 옵션 및 기타 빌드 도구입니다.

[C/c + + 전처리기 참조](../preprocessor/c-cpp-preprocessor-reference.md) pragma, 전처리기 지시문, 미리 정의 된 매크로 및 전처리기에 대 한 자료를 참조 합니다.

[Visual c + + 라이브러리](../standard-library/cpp-standard-library-reference.md) 참조에 대 한 링크 목록이 다양 한 Visual c + + 라이브러리에 대 한 페이지를 시작 합니다.

## <a name="see-also"></a>참고자료

[C# 언어 참조](../c-language/c-language-reference.md)