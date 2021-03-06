---
title: 'Procedura: Modifica del ritardo del componente di descrizione comando di Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolTip component [Windows Forms], delay values
- tooltips [Windows Forms], delay values
- examples [Windows Forms], tooltips
ms.assetid: 08979ba7-dd84-477b-ab17-8d06e759be99
ms.openlocfilehash: 494691a6f91a58f2689c1668d95b2df581b76d79
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54593901"
---
# <a name="how-to-change-the-delay-of-the-windows-forms-tooltip-component"></a>Procedura: Modifica del ritardo del componente di descrizione comando di Windows Form
Sono presenti più valori di ritardo che è possibile impostare per un controllo Windows Form <xref:System.Windows.Forms.ToolTip> componente. L'unità di misura per tutte queste proprietà è millisecondi. Il <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> proprietà determina quanto tempo l'utente deve fare riferimento al controllo associato per la stringa di descrizione comando da visualizzare. Il <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> proprietà imposta il numero di millisecondi impiegato per le stringhe di descrizione comando successive da visualizzare quando il mouse viene spostato da un controllo descrizione comando associato a un altro. Il <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> proprietà determina il periodo di tempo viene visualizzata la stringa di descrizione comando. È possibile impostare questi valori singolarmente o impostando il valore della <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> proprietà; il ritardo di proprietà vengono impostate in base al valore assegnato al <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> proprietà. Ad esempio, quando <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> è impostata su un valore N, <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> è impostato per N, <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> è impostata sul valore di <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> diviso per cinque (o N/5), e <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> è impostata su un valore che è cinque volte il valore della <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> proprietà (o n5).  
  
### <a name="to-set-the-delay"></a>Per impostare il ritardo  
  
1.  Impostare le proprietà seguenti come illustrato in questo esempio.  
  
    ```vb  
    ToolTip1.InitialDelay = 500  
    ToolTip1.ReshowDelay = 100  
    ToolTip1.AutoPopDelay = 5000  
    ```  
  
    ```csharp  
    ToolTip1.InitialDelay = 500;  
    ToolTip1.ReshowDelay = 100;  
    ToolTip1.AutoPopDelay = 5000;  
    ```  
  
    ```cpp  
    toolTip1->InitialDelay = 500;  
    toolTip1->ReshowDelay = 100;  
    toolTip1->AutoPopDelay = 5000;  
    ```  
  
## <a name="see-also"></a>Vedere anche
- [Panoramica sul componente ToolTip](../../../../docs/framework/winforms/controls/tooltip-component-overview-windows-forms.md)
- [Procedura: Impostare le descrizioni comandi per i controlli in un Windows Form in fase di progettazione](../../../../docs/framework/winforms/controls/how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md)
- [Componente ToolTip](../../../../docs/framework/winforms/controls/tooltip-component-windows-forms.md)
