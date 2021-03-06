---
title: SqlChars.Stream 属性 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlChars.Stream
- System.Data.SqlTypes.SqlChars.get_Stream
- System.Data.SqlTypes.SqlChars.set_Stream
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: d756b78a7cdbc12562e474ca3d2c9a1f3529f6bf
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/11/2019
ms.locfileid: "54223047"
---
# <a name="sqlcharsstream-property"></a>SqlChars.Stream 属性

获取或设置字符流。 包含此属性的程序集具有与 SQLAccess.dll 友元关系。 它被用于 SQL server 上。 对于其他数据库，使用提供该数据库的宿主机制。

```csharp
internal SqlStreamChars Stream { get; set; }
```

## <a name="property-value"></a>属性值

`System.Data.SqlTypes.SqlStreamChars`\
字符流中。

## <a name="remarks"></a>备注

> [!WARNING]
> `SqlChars.Stream`属性内部使用并且不应在代码中直接使用。
>
> Microsoft 不支持在生产应用程序在任何情况下使用此属性。

## <a name="requirements"></a>要求

**Namespace**：<xref:System.Data.SqlTypes>

**程序集：** System.Data （在 System.Data.dll 中)

**.NET framework 版本：** 自 2.0 之后可用。