---
title: 'Procedura: Impostare la modalità di ordinamento delle colonne nel controllo DataGridView Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sorting [Windows Forms], data grids
- DataGridView control [Windows Forms], sort mode
- data grids [Windows Forms], sorting data
ms.assetid: 57dfed60-a608-40d5-86f9-d65686ffb325
ms.openlocfilehash: 43ee1f43dfed0a9612ef0b460e5633262c9b6a5c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674885"
---
# <a name="how-to-set-the-sort-modes-for-columns-in-the-windows-forms-datagridview-control"></a>Procedura: Impostare la modalità di ordinamento delle colonne nel controllo DataGridView Windows Form
Nel <xref:System.Windows.Forms.DataGridView> le colonne di caselle di testo di controllo, utilizzano l'ordinamento automatico per impostazione predefinita, mentre altri tipi di colonna non sono ordinati automaticamente. In alcuni casi si dovranno eseguire l'override di questi valori predefiniti. Ad esempio, è possibile visualizzare le immagini al posto di testo, numeri o valori di cella di enumerazione. Mentre le immagini non possono essere ordinate, possono essere ordinati i valori sottostanti che rappresentano.  
  
 Nel <xref:System.Windows.Forms.DataGridView> (controllo), il <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> valore della proprietà di una colonna determina il comportamento di ordinamento.  
  
 La procedura seguente viene illustrato il `Priority` colonna da [come: Personalizzare la formattazione dei dati nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md). Questa colonna è una colonna di immagine e non è ordinabile per impostazione predefinita. Contiene valori di cella effettivo sono stringhe, tuttavia, in modo che possono essere ordinato automaticamente.  
  
### <a name="to-set-the-sort-mode-for-a-column"></a>Per impostare la modalità di ordinamento per una colonna  
  
-   Impostare la proprietà <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A?displayProperty=nameWithType>.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#066](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#066)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#066](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#066)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Un controllo <xref:System.Windows.Forms.DataGridView> denominato `dataGridView1` contenente una colonna denominata `Priority`.  
  
-   Riferimenti agli assembly <xref:System?displayProperty=nameWithType> e <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A?displayProperty=nameWithType>
- [Ordinamento di dati nel controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/sorting-data-in-the-windows-forms-datagridview-control.md)
- [Modalità di ordinamento delle colonne nel controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/column-sort-modes-in-the-windows-forms-datagridview-control.md)
- [Procedura: Personalizzare l'ordinamento nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/how-to-customize-sorting-in-the-windows-forms-datagridview-control.md)
