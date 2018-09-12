---
title: file_status 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 09/10/2018
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- filesystem/std::experimental::filesystem::file_status
- filesystem/std::experimental::filesystem::file_status::operator=
- filesystem/std::experimental::filesystem::file_status::type
- filesystem/std::experimental::filesystem::file_status::permissions
dev_langs:
- C++
ms.assetid: 9781840e-ad22-44dd-ad79-0fabaa94bac4
author: corob-msft
ms.author: corob
helpviewer_keywords:
- std::experimental::filesystem::file_status
- std::experimental::filesystem::file_status::operator=
- std::experimental::filesystem::file_status::type
- std::experimental::filesystem::file_status::permissions
ms.workload:
- cplusplus
ms.openlocfilehash: cc45e785b6a3aeefd9e2cf5d0539b5d387af7143
ms.sourcegitcommit: fb9448eb96c6351a77df04af16ec5c0fb9457d9e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44691668"
---
# <a name="filestatus-class"></a>file_status 클래스

[file_type](../standard-library/filesystem-enumerations.md#file_type) 및 파일 [perms](../standard-library/filesystem-enumerations.md#perms)를 래핑합니다.

## <a name="syntax"></a>구문

```cpp
class file_status;
```

### <a name="constructors"></a>생성자

|생성자|설명|
|-|-|
|[file_status](#file_status)|에 대 한 래퍼를 생성 [file_type](../standard-library/filesystem-enumerations.md#file_type) 파일과 [perms](../standard-library/filesystem-enumerations.md#perms)합니다.|

### <a name="member-functions"></a>멤버 함수

|멤버 함수|설명|
|-|-|
|[type](#type)|`file_type`를 가져오거나 설정합니다.|
|[permissions](#permissions)|파일 사용 권한을 가져오거나 설정합니다.|

### <a name="operators"></a>연산자

|연산자|설명|
|-|-|
|[operator=](#op_as)|기본 멤버 대입 연산자가 예상대로 작동합니다.|

## <a name="requirements"></a>요구 사항

**헤더:** \<파일 시스템 >

**Namespace:** std::experimental::filesystem, std::experimental::filesystem

## <a name="file_status"></a> file_status:: file_status

에 대 한 래퍼를 생성 [file_type](../standard-library/filesystem-enumerations.md#file_type) 파일과 [perms](../standard-library/filesystem-enumerations.md#perms)합니다.

```cpp
explicit file_status(
   file_type ftype = file_type::none,
   perms mask = perms::unknown) noexcept;

file_status(const file_status&) noexcept = default;

file_status(file_status&&) noexcept = default;

~file_status() noexcept = default;
```

### <a name="parameters"></a>매개 변수

*ftype*<br/>
지정 된 `file_type`, 기본값은 `file_type::none`합니다.

*마스크*<br/>
지정 된 파일 `perms`, 기본값은 `perms::unknown`합니다.

*file_status*<br/>
저장 된 개체입니다.

## <a name="op_as"></a> file_status::operator =

기본 멤버 대입 연산자가 예상대로 작동합니다.

```cpp
file_status& operator=(const file_status&) noexcept = default;
file_status& operator=(file_status&&) nexcept = default;
```

### <a name="parameters"></a>매개 변수

*file_status*<br/>
합니다 [file_status](../standard-library/file-status-class.md) 에 복사 되는 `file_status`합니다.

## <a name="type"></a> 형식

`file_type`를 가져오거나 설정합니다.

```cpp
file_type type() const noexcept
void type(file_type ftype) noexcept
```

### <a name="parameters"></a>매개 변수

*ftype*<br/>
`file_type`로 지정됩니다.

## <a name="permissions"></a> 사용 권한

파일 사용 권한을 가져오거나 설정합니다.

Setter를 사용 하 여 파일을 만들어 `readonly` 제거 또는 `readonly` 특성입니다.

```cpp
perms permissions() const noexcept
void permissions(perms mask) noexcept
```

### <a name="parameters"></a>매개 변수

*마스크*<br/>
`perms`로 지정됩니다.

## <a name="see-also"></a>참고자료

[헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)<br/>
[path 클래스](../standard-library/path-class.md)<br/>
[\<filesystem>](../standard-library/filesystem.md)<br/>
