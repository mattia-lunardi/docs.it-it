---
title: 'Procedura: Convalidare i dati nel controllo DataGridView Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], validation
- DataGridView control [Windows Forms], data validation
- data grids [Windows Forms], validating data
- data validation [Windows Forms], Windows Forms
ms.assetid: d10aef35-701e-4a3c-a684-2a2ed1aeaca6
ms.openlocfilehash: 10cd8a0bd2bed7c55be9540d5ee68b13dcd5f90d
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2019
ms.locfileid: "56261726"
---
# <a name="how-to-validate-data-in-the-windows-forms-datagridview-control"></a>Procedura: Convalidare i dati nel controllo DataGridView Windows Form
Nell'esempio di codice seguente viene illustrato come convalidare i dati immessi da un utente in un controllo <xref:System.Windows.Forms.DataGridView>. In questo esempio il controllo <xref:System.Windows.Forms.DataGridView> viene compilato con righe della tabella `Customers` del database di esempio Northwind. Quando l'utente modifica una cella nella colonna `CompanyName`, viene verificato che il valore non sia vuoto e che sia valido. Se il gestore dell'evento <xref:System.Windows.Forms.DataGridView.CellValidating> rileva che il valore è una stringa vuota, il controllo <xref:System.Windows.Forms.DataGridView> impedisce all'utente di uscire dalla cella fino a quando non immette una stringa non vuota.  
  
 Per una spiegazione completa di questo esempio di codice, vedere [procedura dettagliata: Convalida dei dati in di Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).  
  
## <a name="example"></a>Esempio  
 [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#00](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewDataValidation#00](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#00)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Riferimenti agli assembly System, System.Data, System.Windows.Forms e System.XML.  
  
 Per informazioni sulla compilazione di questo esempio dalla riga di comando per Visual Basic o Visual c#, vedere [compilazione dalla riga di comando](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oppure [con la creazione della riga di comando csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). È anche possibile compilare questo esempio in Visual Studio incollando il codice in un nuovo progetto.  
  
## <a name="net-framework-security"></a>Sicurezza di .NET Framework  
 L'archiviazione delle informazioni riservate, ad esempio la password, nella stringa di connessione può avere implicazioni sulla sicurezza dell'applicazione. L'autenticazione di Windows, detta anche sicurezza integrata, consente di controllare l'accesso a un database in modo più sicuro. Per altre informazioni, vedere [Protezione delle informazioni di connessione](../../../../docs/framework/data/adonet/protecting-connection-information.md).  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [Procedura dettagliata: La convalida dei dati nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [Immissione di dati nel controllo DataGridView di Windows Form](../../../../docs/framework/winforms/controls/data-entry-in-the-windows-forms-datagridview-control.md)
- [Procedura dettagliata: Gestione degli errori che si verificano durante l'immissione di dati nel controllo DataGridView Windows Form](../../../../docs/framework/winforms/controls/handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [Protezione delle informazioni di connessione](../../../../docs/framework/data/adonet/protecting-connection-information.md)
