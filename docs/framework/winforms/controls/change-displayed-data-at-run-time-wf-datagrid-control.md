---
title: 'Procedura: Modificare i dati visualizzati in fase di esecuzione nel controllo DataGrid Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DataGrid control [Windows Forms], dynamically changing at run time
- DataGrid control [Windows Forms], data binding
- cells [Windows Forms], changing DataGrid cell values
ms.assetid: 0c7a6d00-30de-416e-8223-0a81ddb4c1f8
ms.openlocfilehash: fc0fe47d728a196de81f7bf099e3a25ac2bb9211
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54605565"
---
# <a name="how-to-change-displayed-data-at-run-time-in-the-windows-forms-datagrid-control"></a>Procedura: Modificare i dati visualizzati in fase di esecuzione nel controllo DataGrid Windows Form
> [!NOTE]
>  Benché il controllo <xref:System.Windows.Forms.DataGridView> sostituisca il controllo <xref:System.Windows.Forms.DataGrid> aggiungendovi funzionalità, il controllo <xref:System.Windows.Forms.DataGrid> viene mantenuto per compatibilità con le versioni precedenti e per un eventuale uso futuro. Per altre informazioni, vedere [Differenze tra i controlli DataGridView e DataGrid Windows Form](../../../../docs/framework/winforms/controls/differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Dopo aver creato un controllo Windows Form <xref:System.Windows.Forms.DataGrid> usando le funzionalità in fase di progettazione, è anche possibile modificare dinamicamente gli elementi del <xref:System.Data.DataSet> oggetti della griglia in fase di esecuzione. Può includere le modifiche dei singoli valori di tabella o la modifica origine dati a cui è associata il <xref:System.Windows.Forms.DataGrid> controllo. Vengono apportate modifiche ai singoli valori tramite il <xref:System.Data.DataSet> dell'oggetto, non il <xref:System.Windows.Forms.DataGrid> controllo.  
  
### <a name="to-change-data-programmatically"></a>Per modificare i dati a livello di codice  
  
1.  Specificare la tabella desiderata di <xref:System.Data.DataSet> oggetto e il valore desiderato di righe e campo dalla tabella e impostare la cella uguale a quello nuovo.  
  
    > [!NOTE]
    >  Per specificare la tabella prima di <xref:System.Data.DataSet> o la prima riga della tabella, usare 0.  
  
     Nell'esempio seguente viene illustrato come modificare la seconda voce della prima riga della tabella prima di un set di dati, fare clic su `Button1`. Il <xref:System.Data.DataSet> (`ds`) e le tabelle (`0` e `1`) creati in precedenza.  
  
    ```vb  
    Protected Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       ds.tables(0).rows(0)(1) = "NewEntry"  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       ds.Tables[0].Rows[0][1]="NewEntry";  
    }  
    ```  
  
    ```cpp  
    private:   
       void button1_Click(System::Object^ sender, System::EventArgs^ e)  
       {  
          dataSet1->Tables[0]->Rows[0][1] = "NewEntry";  
       }  
    ```  
  
     (Visual c#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) inserire il codice seguente nel costruttore del form per registrare il gestore dell'evento.  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click +=  
       gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
     In fase di esecuzione è possibile usare la <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> metodo a cui associare il <xref:System.Windows.Forms.DataGrid> controllo a un'origine dati diversa. Ad esempio, si possono invece avere diversi [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)] controlli dei dati, ciascuna connessa a un database diverso.  
  
### <a name="to-change-the-datasource-programmatically"></a>Per modificare l'origine dati a livello di codice  
  
1.  Impostare il <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> al nome dell'origine dati e della tabella che si desidera associare al metodo.  
  
     Nell'esempio seguente viene illustrato come modificare l'origine dati utilizzando il <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> metodo a un [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)] controllo dati (adoPubsAuthors) che è connessa alla tabella Authors nel database Pubs.  
  
    ```vb  
    Private Sub ResetSource()  
       DataGrid1.SetDataBinding(adoPubsAuthors, "Authors")  
    End Sub  
    ```  
  
    ```csharp  
    private void ResetSource()  
    {  
       DataGrid1.SetDataBinding(adoPubsAuthors, "Authors");  
    }  
    ```  
  
    ```cpp  
    private:  
       void ResetSource()  
       {  
          dataGrid1->SetDataBinding(adoPubsAuthors, "Authors");  
       }  
    ```  
  
## <a name="see-also"></a>Vedere anche
- [Oggetti DataSet ADO.NET](../../../../docs/framework/data/adonet/ado-net-datasets.md)
- [Procedura: Eliminare o nascondere colonne nel controllo DataGrid Windows Form](../../../../docs/framework/winforms/controls/how-to-delete-or-hide-columns-in-the-windows-forms-datagrid-control.md)
- [Procedura: Aggiungere tabelle e colonne al controllo DataGrid Windows Form](../../../../docs/framework/winforms/controls/how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)
- [Procedura: Associare il controllo DataGrid di Windows Form a un'origine dati](../../../../docs/framework/winforms/controls/how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md)
