---
title: 'Procedura: Creare ListViewItems con un CheckBox'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], ListView
- controls [WPF], CheckBox
- ListView controls [WPF], CheckBox controls
- CheckBox control [WPF], ListView control
ms.assetid: f6d66c7f-906c-4f65-a55a-0ede9d00e26a
ms.openlocfilehash: 1ed623495529609c83c0ced68bfc1696c29d4570
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54682242"
---
# <a name="how-to-create-listviewitems-with-a-checkbox"></a>Procedura: Creare ListViewItems con un CheckBox
Questo esempio viene illustrato come visualizzare una colonna <xref:System.Windows.Controls.CheckBox> controlli in un <xref:System.Windows.Controls.ListView> controllo che usa un <xref:System.Windows.Controls.GridView>.  
  
## <a name="example"></a>Esempio  
 Per creare una colonna che contiene <xref:System.Windows.Controls.CheckBox> controlli in un <xref:System.Windows.Controls.ListView>, creare un <xref:System.Windows.DataTemplate> che contiene un <xref:System.Windows.Controls.CheckBox>. Impostare quindi la <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> di un <xref:System.Windows.Controls.GridViewColumn> per il <xref:System.Windows.DataTemplate>.  
  
 L'esempio seguente mostra una <xref:System.Windows.DataTemplate> che contiene un <xref:System.Windows.Controls.CheckBox>. Nell'esempio viene associato il <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> proprietà del <xref:System.Windows.Controls.CheckBox> per il <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> valore della proprietà di <xref:System.Windows.Controls.ListViewItem> che lo contiene. Pertanto, quando la <xref:System.Windows.Controls.ListViewItem> che contiene il <xref:System.Windows.Controls.CheckBox> è selezionata, il <xref:System.Windows.Controls.CheckBox> sia selezionata.  
  
 [!code-xaml[ListViewChkBox#CheckBoxDataTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#checkboxdatatemplate)]  
  
 Nell'esempio seguente viene illustrato come creare una colonna di <xref:System.Windows.Controls.CheckBox> controlli. Impostare la colonna, nell'esempio viene impostata la <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> proprietà del <xref:System.Windows.Controls.GridViewColumn> per il <xref:System.Windows.DataTemplate>.  
  
 [!code-xaml[ListViewChkBox#GridViewColumnCheckBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#gridviewcolumncheckbox)]  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Panoramica sul controllo ListView](../../../../docs/framework/wpf/controls/listview-overview.md)
- [Procedure relative alle proprietà](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [Cenni preliminari su GridView](../../../../docs/framework/wpf/controls/gridview-overview.md)
