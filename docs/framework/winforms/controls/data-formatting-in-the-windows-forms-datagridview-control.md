---
title: Formattazione di dati nel controllo DataGridView di Windows Form
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting data
- data [Windows Forms], formatting in grids
- data grids [Windows Forms], formatting data
ms.assetid: 07bf558d-3748-42ba-8ba0-37fdef924081
ms.openlocfilehash: 0016b87add6f20223bdeda72f10ac94b74ec9fcf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737858"
---
# <a name="data-formatting-in-the-windows-forms-datagridview-control"></a>Formattazione di dati nel controllo DataGridView di Windows Form
Il <xref:System.Windows.Forms.DataGridView> controllo fornisce la conversione automatica tra i tipi di dati che consentono di visualizzare le colonne padre e i valori delle celle. Le colonne di caselle di testo, ad esempio, visualizzare le rappresentazioni di stringa di data, ora, numero e i valori di enumerazione e convertire i valori stringa immessi dall'utente per i tipi richiesti dall'archivio dati.  
  
## <a name="formatting-with-the-datagridviewcellstyle-class"></a>La formattazione con la classe DataGridViewCellStyle  
 Il <xref:System.Windows.Forms.DataGridView> controllo fornisce la formattazione dei dati di base dei valori di cella attraverso i <xref:System.Windows.Forms.DataGridViewCellStyle> classe. È possibile usare la <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> proprietà su valori di data, ora, numero ed enumerazione formato per la lingua predefinita corrente usando gli specificatori del formato descritto in [formattazione di tipi](../../../../docs/standard/base-types/formatting-types.md). È anche possibile formattare questi valori per le impostazioni cultura specifiche utilizzando il <xref:System.Windows.Forms.DataGridViewCellStyle.FormatProvider%2A> proprietà. Il formato specificato viene usato per visualizzare i dati e analizzare i dati immessi dall'utente nel formato specificato.  
  
 Il <xref:System.Windows.Forms.DataGridViewCellStyle> classe fornisce proprietà di formattazione aggiuntive per ritorno a capo automatico, l'allineamento del testo e la visualizzazione personalizzata dei valori null del database. Per altre informazioni, vedere [Procedura: Formattare i dati nella finestra di Windows Form controllo DataGridView](../../../../docs/framework/winforms/controls/how-to-format-data-in-the-windows-forms-datagridview-control.md).  
  
## <a name="formatting-with-the-cellformatting-event"></a>La formattazione con l'evento CellFormatting  
 Se la formattazione di base non soddisfa le proprie esigenze, è possibile fornire dati personalizzati di formattazione in un gestore per il <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> evento. Il <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs> passati al gestore di è un <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> proprietà che inizialmente contiene il valore della cella. In genere, questo valore viene automaticamente convertito al tipo di visualizzazione. Per convertire il valore, impostare il <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> proprietà su un valore del tipo di visualizzazione.  
  
> [!NOTE]
>  Se una stringa di formato è attiva per la cella, viene eseguito l'override della modifica del <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> valore della proprietà solo se si impostano le <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs.FormattingApplied%2A> proprietà `true`.  
  
 Il <xref:System.Windows.Forms.DataGridView.CellFormatting> eventi sono utili anche quando si desidera impostare <xref:System.Windows.Forms.DataGridViewCellStyle> proprietà per le singole celle in base i relativi valori. Per altre informazioni, vedere [Procedura: Personalizzare la formattazione dei dati nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md).  
  
 Se l'analisi predefinita dei valori specificati dall'utente non soddisfa le proprie esigenze, è possibile gestire il <xref:System.Windows.Forms.DataGridView.CellParsing> eventi del <xref:System.Windows.Forms.DataGridView> controllo per fornire un'analisi personalizzata.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- [Visualizzazione di dati nel controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)
- [Stili delle celle nel controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md)
- [Procedura: Formattare i dati nella finestra di Windows Form controllo DataGridView](../../../../docs/framework/winforms/controls/how-to-format-data-in-the-windows-forms-datagridview-control.md)
- [Procedura: Personalizzare la formattazione dei dati nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)
