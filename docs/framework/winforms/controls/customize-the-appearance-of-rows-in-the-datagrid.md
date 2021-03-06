---
title: 如何：自定义 Windows 窗体 DataGridView 控件中的行的外观
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], customizing rows
- rows [Windows Forms], customizing in DataGridView control
- DataGridView control [Windows Forms], customizing rows
ms.assetid: d40b53d2-7e7c-48c5-8570-6e79d15c3bbb
ms.openlocfilehash: 6ec3765eb667f8a249afa815400eb7f1edbec3dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632941"
---
# <a name="how-to-customize-the-appearance-of-rows-in-the-windows-forms-datagridview-control"></a>如何：自定义 Windows 窗体 DataGridView 控件中的行的外观
通过处理 <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType> 和 <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType> 事件之一或两者同时处理，可以控制 <xref:System.Windows.Forms.DataGridView> 行的外观。 这些事件设计用于使你可以仅绘制想绘制的内容，同时使 <xref:System.Windows.Forms.DataGridView> 控件绘制其余内容。 例如，如果要绘制自定义背景，则可以处理 <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType> 事件并让各个单元格自行绘制自己的前景内容。 或者，还可以让单元格自行绘制，并在 <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType> 事件的处理程序中添加自定义前景内容。 此外，还可以禁用单元格绘制，并在 <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType> 事件处理程序中亲自绘制所有内容。  
  
 下面的代码示例实现两个事件的处理程序，以便提供渐变选区背景和某些跨多个列的自定义前景内容。  
  
## <a name="example"></a>示例  
 [!code-csharp[System.Windows.Forms.DataGridViewRowPainting#00](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRowPainting/CS/datagridviewrowpainting.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewRowPainting#00](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRowPainting/VB/datagridviewrowpainting.vb#00)]  
  
## <a name="compiling-the-code"></a>编译代码  
 此示例需要：  
  
-   对 System、System.Drawing 和 System.Windows.Forms 程序集的引用。  
  
 Visual Basic 或 Visual C# 生成命令行中的此示例的信息，请参阅[从命令行生成](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)或[命令行上使用 csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)。 也可以通过将代码粘贴到新的项目中生成此示例在 Visual Studio 中。  另请参阅[如何：编译和运行完整的 Windows 窗体代码示例使用 Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))。  
  
## <a name="see-also"></a>请参阅
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType>
- [自定义 Windows 窗体 DataGridView 控件](../../../../docs/framework/winforms/controls/customizing-the-windows-forms-datagridview-control.md)
- [DataGridView 控件体系结构](../../../../docs/framework/winforms/controls/datagridview-control-architecture-windows-forms.md)
