---
title: 'Procedura: Nascondere colonne nel controllo DataGridView Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], hiding columns
- data grids [Windows Forms], hiding columns
- columns [Windows Forms], hiding
ms.assetid: 3f94143a-2ef0-49a5-a22a-b2e6f9289642
ms.openlocfilehash: 726fa8ee05498ae365409c8330c6e1d9283ae9f5
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/21/2019
ms.locfileid: "56583271"
---
# <a name="how-to-hide-columns-in-the-windows-forms-datagridview-control"></a>Procedura: Nascondere colonne nel controllo DataGridView Windows Form
A volte può essere necessario visualizzare solo alcune colonne tra quelle disponibili in un controllo <xref:System.Windows.Forms.DataGridView> Windows Form. Ad esempio, può essere necessario mostrare una colonna con gli stipendi dei dipendenti agli utenti con credenziali di gestione e nasconderla invece agli altri utenti. Oppure potrebbe essere necessario associare il controllo a un'origine dati contenente più colonne, di cui solo alcune devono essere visualizzate. In questo caso, si rimuovono in genere le colonne che non interessa visualizzare, invece di nasconderle.  
  
 Nel controllo <xref:System.Windows.Forms.DataGridView>, il valore della proprietà <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A> di una colonna determina se la colonna viene visualizzata.  
  
 Questa attività è supportata in Visual Studio.  Vedere anche [come: Nascondere le colonne in di Windows Form usando la finestra di progettazione di DataGridView Control](hide-columns-in-the-datagrid-using-the-designer.md).  
  
### <a name="to-hide-a-column-programmatically"></a>Per nascondere una colonna a livello di codice  
  
-   Impostare la proprietà <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType> su `false`. Per nascondere una colonna `CustomerID` generata automaticamente durante il data binding, inserire il seguente esempio di codice in un gestore dell'evento <xref:System.Windows.Forms.DataGridView.DataBindingComplete>.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#063](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#063)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#063](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#063)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Un controllo <xref:System.Windows.Forms.DataGridView> denominato `dataGridView1` contenente una colonna denominata `CustomerID`.  
  
-   Riferimenti agli assembly <xref:System?displayProperty=nameWithType> e <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType>
- [Funzionalità di base per colonna, riga e cella nel controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)
- [Procedura: Rimuovere le colonne generate automaticamente da un controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/remove-autogenerated-columns-from-a-wf-datagridview-control.md)
- [Procedura: Modificare l'ordine delle colonne nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control.md)
