---
title: Windows 窗体 DataGridView 控件中的性能优化
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], performance tuning
- performance [Windows Forms], DataGridView control
- performance tuning [Windows Forms], data grids
ms.assetid: 6ccbff28-a0ff-41e4-b601-61b31b61851d
ms.openlocfilehash: 556e3f682b6b863f8ab350c1b8ca7409a04a94fc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729026"
---
# <a name="performance-tuning-in-the-windows-forms-datagridview-control"></a>Windows 窗体 DataGridView 控件中的性能优化
当使用大量的数据，`DataGridView`控件可以消耗大量的内存开销，除非谨慎使用。 在内存有限的客户端，可以避免此开销的一些通过避免具有高内存成本的功能。 你还可以管理部分或全部数据维护和检索任务自己使用的虚拟模式以自定义你的方案的内存使用情况。  
  
## <a name="in-this-section"></a>本节内容  
 [有关缩放 Windows 窗体 DataGridView 控件的最佳做法](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md)  
 介绍如何使用`DataGridView`中来避免不必要的内存使用情况和性能损失，处理大量数据时的控件。  
  
 [Windows 窗体 DataGridView 控件中的虚拟模式](../../../../docs/framework/winforms/controls/virtual-mode-in-the-windows-forms-datagridview-control.md)  
 介绍如何使用虚拟模式下以补充或替代标准的数据绑定机制。  
  
 [演练：在 Windows 窗体 DataGridView 控件中实现虚拟模式](../../../../docs/framework/winforms/controls/implementing-virtual-mode-wf-datagridview-control.md)  
 介绍如何实现虚拟模式下的多个事件的处理程序。 此外演示了如何实现行级回滚和提交用户编辑。  
  
 [在 Windows 窗体 DataGridView 控件中实现实时数据加载的虚拟模式](../../../../docs/framework/winforms/controls/implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)  
 介绍如何加载数据按需、 具有更多可显示与可用的客户端内存可以存储数据时非常有用。  
  
## <a name="reference"></a>参考  
 <xref:System.Windows.Forms.DataGridView>  
 提供关于 <xref:System.Windows.Forms.DataGridView> 控件的参考文档。  
  
 <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>  
 为提供参考文档<xref:System.Windows.Forms.DataGridView.VirtualMode%2A>属性。  
  
## <a name="see-also"></a>请参阅
- [DataGridView 控件](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)
- [Windows 窗体 DataGridView 控件中的数据显示模式](../../../../docs/framework/winforms/controls/data-display-modes-in-the-windows-forms-datagridview-control.md)
