---
title: 无效模式字符串
ms.date: 07/20/2015
ms.assetid: ec1aecdb-5339-4a93-be71-eec56b1d7438
ms.openlocfilehash: 3fa42632ad6d69642d7b8ec36bf2880bc10a5024
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732474"
---
# <a name="invalid-pattern-string"></a>无效模式字符串
在搜索的 `Like` 操作中指定的模式字符串无效。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1.  查看列表中表达式的有效字符。  
  
2.  在模式范围内，请确保起始范围字符小于结束范围字符，如 `[a-z]`中所示。  
  
3.  在模式范围内，请确保不存在彼此相邻的多个连字符，如 `[a--z]`中所示。  
  
4.  以右括号结束模式范围。  
  
## <a name="see-also"></a>请参阅
- [Like 运算符](../../visual-basic/language-reference/operators/like-operator.md)
