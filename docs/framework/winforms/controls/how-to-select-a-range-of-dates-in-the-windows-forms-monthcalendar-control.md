---
title: 'Procedura: Selezionare un intervallo di date nel controllo MonthCalendar Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- dates [Windows Forms], selecting range in calendar controls
- examples [Windows Forms], calendar controls
- calendars [Windows Forms], selecting date range
- MonthCalendar control [Windows Forms], selecting date range
ms.assetid: 95d9ab95-b0f8-4c19-9f63-b5cd4593a5d0
ms.openlocfilehash: 4c7100f77c313d219cfd4cceff5ae3015eae4c18
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558449"
---
# <a name="how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control"></a>Procedura: Selezionare un intervallo di date nel controllo MonthCalendar Windows Form
Una caratteristica importante dei moduli di Windows <xref:System.Windows.Forms.MonthCalendar> controllo è che l'utente può selezionare un intervallo di date. Questa funzionalità è un miglioramento rispetto alla funzionalità di selezione della data del <xref:System.Windows.Forms.DateTimePicker> controllo, che consente solo all'utente di selezionare un valore data/ora singolo. È possibile impostare un intervallo di date oppure ottenere impostato dall'utente utilizzando le proprietà di un intervallo di selezione il <xref:System.Windows.Forms.MonthCalendar> controllo. Esempio di codice seguente viene illustrato come impostare un intervallo di selezione.  
  
### <a name="to-select-a-range-of-dates"></a>Per selezionare un intervallo di date  
  
1.  Creare <xref:System.DateTime> gli oggetti che rappresentano le date e il cognome in un intervallo.  
  
    ```vb  
    Dim projectStart As Date = New DateTime(2001, 2, 13)  
    Dim projectEnd As Date = New DateTime(2001, 2, 28)  
    ```  
  
    ```csharp  
    DateTime projectStart = new DateTime(2001, 2, 13);  
    DateTime projectEnd = new DateTime(2001, 2, 28);  
    ```  
  
    ```cpp  
    DateTime projectStart = DateTime(2001, 2, 13);  
    DateTime projectEnd = DateTime(2001, 2, 28);  
    ```  
  
2.  Impostare la proprietà <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A>.  
  
    ```vb  
    MonthCalendar1.SelectionRange = New SelectionRange(projectStart, projectEnd)  
    ```  
  
    ```csharp  
    monthCalendar1.SelectionRange = new SelectionRange(projectStart, projectEnd);  
    ```  
  
    ```cpp  
    monthCalendar1->SelectionRange = gcnew  
       SelectionRange(projectStart, projectEnd);  
    ```  
  
     - oppure -  
  
     Impostare le proprietà <xref:System.Windows.Forms.MonthCalendar.SelectionStart%2A> e <xref:System.Windows.Forms.MonthCalendar.SelectionEnd%2A>.  
  
    ```vb  
    MonthCalendar1.SelectionStart = projectStart  
    MonthCalendar1.SelectionEnd = projectEnd  
    ```  
  
    ```csharp  
    monthCalendar1.SelectionStart = projectStart;  
    monthCalendar1.SelectionEnd = projectEnd;  
    ```  
  
    ```cpp  
    monthCalendar1->SelectionStart = projectStart;  
    monthCalendar1->SelectionEnd = projectEnd;  
    ```  
  
## <a name="see-also"></a>Vedere anche
- [Controllo MonthCalendar](../../../../docs/framework/winforms/controls/monthcalendar-control-windows-forms.md)
- [Procedura: Modificare l'aspetto del controllo MonthCalendar di Windows Form](../../../../docs/framework/winforms/controls/how-to-change-monthcalendar-control-appearance.md)
- [Procedura: Visualizzare giorni specifici in grassetto con il Windows Form controllo MonthCalendar](../../../../docs/framework/winforms/controls/display-specific-days-in-bold-with-wf-monthcalendar-control.md)
- [Procedura: Visualizzare più mesi nel controllo MonthCalendar Windows Form](../../../../docs/framework/winforms/controls/display-more-than-one-month-wf-monthcalendar-control.md)
