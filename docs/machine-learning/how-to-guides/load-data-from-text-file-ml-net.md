---
title: 从文本文件加载数据以进行机器学习处理 - ML.NET
description: 通过 ML.NET，了解如何从文本文件加载数据用于机器学习模型生成、定型和评分
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 7b1e8d3fb6047059c14ec3db8450364a84497219
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156555"
---
# <a name="load-data-from-a-text-file-for-machine-learning-processing---mlnet"></a>从文本文件加载数据以进行机器学习处理 - ML.NET

`TextLoader` 用于从文本文件加载数据。 需要在文本文件中指定数据列、类型及其位置。

注意，读取文件的某些列或多次读取同一列是完全可以接受的。

[示例文件](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt)：
```
Label   Workclass   education   marital-status
0   Private 11th    Never-married
0   Private HS-grad Married-civ-spouse
1   Local-gov   Assoc-acdm  Married-civ-spouse
1   Private Some-college    Married-civ-spouse
```

从文本文件中加载数据：

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();
TextLoader textLoader;

// Create the reader: define the data columns and where to find them in the text file.
textLoader = mlContext.Data.TextReader(new TextLoader.Arguments()
{
    Separator = ",",
    HasHeader = true,
    Column = new[]
                {
                    new TextLoader.Column("VendorId", DataKind.Text, 0),
                    new TextLoader.Column("RateCode", DataKind.Text, 1),
                    new TextLoader.Column("PassengerCount", DataKind.R4, 2),
                    new TextLoader.Column("TripTime", DataKind.R4, 3),
                    new TextLoader.Column("TripDistance", DataKind.R4, 4),
                    new TextLoader.Column("PaymentType", DataKind.Text, 5),
                    new TextLoader.Column("FareAmount", DataKind.R4, 6)
                }
}
);

// Now read the file (remember though, readers are lazy, so the reading will happen when the data is accessed).
var data = textLoader.Read(dataPath);
```