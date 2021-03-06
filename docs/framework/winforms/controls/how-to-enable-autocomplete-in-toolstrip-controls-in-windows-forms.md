---
title: 如何：在 Windows 窗体的 ToolStrip 控件中启用自动完成
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- AutoComplete [Windows Forms], examples
- toolbars [Windows Forms], AutoComplete
- examples [Windows Forms], toolbars
- AutoComplete [Windows Forms], enabling in toolbars
- ToolStripComboBox class [Windows Forms], examples
- ToolStrip control [Windows Forms], AutoComplete
ms.assetid: fd66d085-1af1-45d4-930a-cde944da2e16
ms.openlocfilehash: cc3ec2dd0bdd7f83b2cd6b8cfaf0cad37238707b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514811"
---
# <a name="how-to-enable-autocomplete-in-toolstrip-controls-in-windows-forms"></a>如何：在 Windows 窗体的 ToolStrip 控件中启用自动完成
以下过程将合并<xref:System.Windows.Forms.ToolStripLabel>与<xref:System.Windows.Forms.ToolStripComboBox>，可以删除最近如显示的项，列表访问的网站。 如果用户键入匹配某一项在列表中的第一个字符的字符，会立即显示项。  
  
> [!NOTE]
>  自动完成适用于`ToolStrip`它如适用于传统控件的同一方法中的控件<xref:System.Windows.Forms.ComboBox>和<xref:System.Windows.Forms.TextBox>。  
  
### <a name="to-enable-autocomplete-in-a-toolstrip-control"></a>若要在 ToolStrip 控件中启用自动完成  
  
1.  创建<xref:System.Windows.Forms.ToolStrip>控制并向其添加项。  
  
    ```vb  
    ToolStrip1 = New System.Windows.Forms.ToolStrip  
    ToolStrip1.Items.AddRange(New System.Windows.Forms.ToolStripItem()_  
        {ToolStripLabel1, ToolStripComboBox1})  
    ```  
  
    ```csharp  
    toolStrip1 = new System.Windows.Forms.ToolStrip();  
    toolStrip1.Items.AddRange(new System.Windows.Forms.ToolStripItem[]   
        {toolStripLabel1, toolStripComboBox1});  
    ```  
  
2.  设置<xref:System.Windows.Forms.ToolStripItem.Overflow%2A>属性的标签，并向组合框<xref:System.Windows.Forms.ToolStripItemOverflow.Never>，以便列表始终是无论窗体的大小。  
  
    ```vb  
    ToolStripLabel1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    ToolStripComboBox1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    ```  
  
    ```csharp  
    toolStripLabel1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    toolStripComboBox1.Overflow = System.Windows.Forms.ToolStripItemOverflow.Never  
    ```  
  
3.  将字添加到的项集合<xref:System.Windows.Forms.ToolStripComboBox>控件。  
  
    ```vb  
    ToolStripComboBox1.Items.AddRange(New Object() {"First Item", _  
        "Second Item", "Third Item"})  
    ```  
  
    ```csharp  
    toolStripComboBox1.Items.AddRange(new object[] {"First item", "Second item", "Third item"});  
    ```  
  
4.  设置<xref:System.Windows.Forms.ComboBox.AutoCompleteMode%2A>属性的组合框<xref:System.Windows.Forms.AutoCompleteMode.Append>。  
  
    ```vb  
    ToolStripComboBox1.AutoCompleteMode = _  
        System.Windows.Forms.AutoCompleteMode.Append  
    ```  
  
    ```csharp  
    toolStripComboBox1.AutoCompleteMode = System.Windows.Forms.AutoCompleteMode.Append;  
    ```  
  
5.  设置<xref:System.Windows.Forms.ComboBox.AutoCompleteSource%2A>属性的组合框<xref:System.Windows.Forms.AutoCompleteSource.ListItems>。  
  
    ```vb  
    ToolStripComboBox1.AutoCompleteSource = _  
        System.Windows.Forms.AutoCompleteSource.ListItems  
    ```  
  
    ```csharp  
    toolStripComboBox1.AutoCompleteSource = System.Windows.Forms.AutoCompleteSource.ListItems;  
    ```  
  
## <a name="see-also"></a>请参阅
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripLabel>
- <xref:System.Windows.Forms.ToolStripComboBox>
- <xref:System.Windows.Forms.ToolStripComboBox.AutoCompleteMode%2A>
- <xref:System.Windows.Forms.ToolStripComboBox.AutoCompleteSource%2A>
- [ToolStrip 控件概述](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
- [ToolStrip 控件体系结构](../../../../docs/framework/winforms/controls/toolstrip-control-architecture.md)
- [ToolStrip 技术摘要](../../../../docs/framework/winforms/controls/toolstrip-technology-summary.md)
