---
title: 如何：将过程传递给 Visual Basic 中的另一个过程
ms.date: 07/20/2015
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- delegates [Visual Basic], passing procedures
ms.assetid: 5adbba15-5a1d-413f-ab3e-3ff6cc0a4669
ms.openlocfilehash: cf5a8447cbedcd8071da98ac6763ff06eb608199
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506753"
---
# <a name="how-to-pass-procedures-to-another-procedure-in-visual-basic"></a>如何：将过程传递给 Visual Basic 中的另一个过程
此示例演示如何使用委托来将过程传递给另一个过程。  
  
 委托是可以使用类似于在 Visual Basic 中的任何其他类型的类型。 `AddressOf`运算符返回的委托对象时应用于过程名称。  
  
 此示例中有一个具有一个委托参数，可能需要对另一个过程，获得的引用过程`AddressOf`运算符。  
  
### <a name="create-the-delegate-and-matching-procedures"></a>创建委托和匹配过程  
  
1.  创建名为的委托`MathOperator`。  
  
     [!code-vb[VbVbalrDelegates#1](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_1.vb)]  
  
2.  创建一个名为过程`AddNumbers`使用参数和返回值相匹配的`MathOperator`，以便签名匹配。  
  
     [!code-vb[VbVbalrDelegates#2](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_2.vb)]  
  
3.  创建一个名为过程`SubtractNumbers`相匹配的签名与`MathOperator`。  
  
     [!code-vb[VbVbalrDelegates#3](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_3.vb)]  
  
4.  创建一个名为过程`DelegateTest`采用委托作为参数。  
  
     此过程可以接受的引用`AddNumbers`或`SubtractNumbers`，因为它们的签名匹配`MathOperator`签名。  
  
     [!code-vb[VbVbalrDelegates#4](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_4.vb)]  
  
5.  创建一个名为过程`Test`的调用`DelegateTest`一次使用的委托`AddNumbers`作为参数，并再次使用的委托`SubtractNumbers`作为参数。  
  
     [!code-vb[VbVbalrDelegates#5](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_5.vb)]  
  
     当`Test`是其调用，首先显示的结果`AddNumbers`作用于`5`和`3`，也就是 8。 然后的结果`SubtractNumbers`对操作`9`和`3`显示，则其为 6。  
  
## <a name="see-also"></a>请参阅
- [委托](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [AddressOf 运算符](../../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Delegate 语句](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [如何：调用委托方法](../../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)
