---
title: 'Procedura: Visualizzare immagini in celle del controllo DataGridView Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cells [Windows Forms], displaying images
- data grids [Windows Forms], displaying in grids
- DataGridView control [Windows Forms], displaying images
- data grids [Windows Forms], displaying images in cells
ms.assetid: 53b13d31-1b56-476d-9ab4-18bfac138a22
ms.openlocfilehash: 637cb2f51e8ad1161b0208a3ebd8337859261a11
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54523597"
---
# <a name="how-to-display-images-in-cells-of-the-windows-forms-datagridview-control"></a>Procedura: Visualizzare immagini in celle del controllo DataGridView Windows Form
E un'immagine è uno dei valori che è possibile visualizzare in una riga di dati. Spesso, questi elementi grafici assumono la forma della fotografia di un dipendente o un logo aziendale.  
  
 L'inserimento delle immagini è semplice quando si visualizzano i dati all'interno di <xref:System.Windows.Forms.DataGridView> controllo. Il <xref:System.Windows.Forms.DataGridView> qualsiasi formato di immagine supportato da e gestisce in modo nativo il <xref:System.Drawing.Image> formato utilizzato da alcuni database dell'immagine di classe, nonché di OLE.  
  
 Se il <xref:System.Windows.Forms.DataGridView> origine dati del controllo ha una colonna di immagini, questi verranno visualizzati automaticamente dal <xref:System.Windows.Forms.DataGridView> controllo.  
  
 Esempio di codice seguente viene illustrato come estrarre un'icona da una risorsa incorporata e convertirlo in una bitmap da visualizzare in ogni cella della colonna di tipo image. Per un altro esempio che sostituisce i valori delle celle testuali con immagini corrispondenti, vedere [come: Personalizzare la formattazione dei dati nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md).  
  
## <a name="example"></a>Esempio  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#050](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#050)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#050](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#050)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Un controllo <xref:System.Windows.Forms.DataGridView> denominato `dataGridView1`.  
  
-   Una risorsa icona incorporata denominata `tree.ico`.  
  
-   Riferimenti agli assembly <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType> e <xref:System.Drawing?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.DataGridView>
- [Funzionalità di base per colonna, riga e cella nel controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)
- [Procedura: Personalizzare la formattazione dei dati nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)
