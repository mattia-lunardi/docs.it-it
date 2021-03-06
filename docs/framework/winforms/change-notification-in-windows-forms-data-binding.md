---
title: Notifica delle modifiche nel data binding dei Windows Form
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, data binding
- Windows Forms, adding change notification for data binding
ms.assetid: b5b10f90-0585-41d9-a377-409835262a92
ms.openlocfilehash: 533bda1e08d2ed7d15160318e75f2c1b7224d989
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505900"
---
# <a name="change-notification-in-windows-forms-data-binding"></a>Notifica delle modifiche nel data binding dei Windows Form
Uno dei principali concetti di data binding in Windows Form consiste *notifica delle modifiche*. Per assicurarsi che l'origine dati e i controlli associati dispongano sempre dei dati più recenti, è necessario aggiungere la notifica delle modifiche per il data binding. In particolare, per assicurarsi che i controlli associati vengono notificati le modifiche apportate all'origine dati e l'origine dati viene informato delle modifiche apportate alle proprietà di un controllo associata.  
  
 Esistono diversi tipi di notifica delle modifiche, a seconda del tipo di associazione dati:  
  
-   Associazione semplice, in cui la proprietà di un singolo controllo è associata a una singola istanza di un oggetto.  
  
-   Associazione basato su elenchi, che può includere una proprietà del controllo singolo associata alla proprietà di un elemento in un elenco o una proprietà del controllo associato a un elenco di oggetti.  
  
 Inoltre, se si siano creando i controlli Windows Form che si desidera utilizzare per il data binding, è necessario applicare il *PropertyName*modificata modello ai controlli, in modo che le modifiche alla proprietà associata di un controllo vengono propagate le origine dati.  
  
## <a name="change-notification-for-simple-binding"></a>Notifica delle modifiche per l'associazione semplice  
 Per l'associazione semplice, oggetti business devono fornire la notifica di modifica quando cambia il valore di una proprietà associata. È possibile farlo tramite l'esposizione di un *PropertyName*Changed per ogni proprietà dell'oggetto business e binding dell'oggetto business a controlli con il <xref:System.Windows.Forms.BindingSource> o il metodo preferito in cui l'oggetto di business implementa il <xref:System.ComponentModel.INotifyPropertyChanged> interfaccia e genera un <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> evento quando cambia il valore di una proprietà. Per altre informazioni, vedere [Procedura: Implementare l'interfaccia INotifyPropertyChanged](../../../docs/framework/winforms/how-to-implement-the-inotifypropertychanged-interface.md). Quando si usano gli oggetti che implementano il <xref:System.ComponentModel.INotifyPropertyChanged> interfaccia, non è necessario usare il <xref:System.Windows.Forms.BindingSource> per associare l'oggetto a un controllo, ma tramite il <xref:System.Windows.Forms.BindingSource> è consigliato.  
  
## <a name="change-notification-for-list-based-binding"></a>Notifica delle modifiche per l'associazione basata su elenchi  
 Windows Form dipende da un elenco associato a modifiche delle proprietà (cambia di valore della proprietà elemento elenco) e l'elenco modificato (un elemento viene eliminato o aggiunto all'elenco) le informazioni per i controlli associati. Pertanto, è necessario implementare gli elenchi usati per il data binding di <xref:System.ComponentModel.IBindingList>, che offre entrambi i tipi di notifica delle modifiche. Il <xref:System.ComponentModel.BindingList%601> è un'implementazione generica dello <xref:System.ComponentModel.IBindingList> ed è progettato per l'uso con data binding in Windows Form. È possibile creare un <xref:System.ComponentModel.BindingList%601> che contiene un tipo di oggetto business che implementa <xref:System.ComponentModel.INotifyPropertyChanged> e l'elenco verrà convertita automaticamente le <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> eventi <xref:System.ComponentModel.IBindingList.ListChanged> eventi. Se l'elenco associato non è un <xref:System.ComponentModel.IBindingList>, è necessario associare l'elenco di oggetti a controlli Windows Form usando la <xref:System.Windows.Forms.BindingSource> componente. Il <xref:System.Windows.Forms.BindingSource> componente fornirà conversione a-elenco di proprietà simile a quella del <xref:System.ComponentModel.BindingList%601>. Per altre informazioni, vedere [Procedura: Generare notifiche di modifica utilizzando un BindingSource e l'interfaccia INotifyPropertyChanged](../../../docs/framework/winforms/controls/raise-change-notifications--bindingsource.md).  
  
## <a name="change-notification-for-custom-controls"></a>Notifica di modifica per i controlli personalizzati  
 Infine, dal lato del controllo è necessario esporre un *PropertyName*evento Changed per ogni proprietà progettate per essere associato a dati. Le modifiche alla proprietà del controllo vengono propagate all'origine dati associata. Per altre informazioni, vedere [Procedura: Applicare il modello PropertyNameChanged](../../../docs/framework/winforms/how-to-apply-the-propertynamechanged-pattern.md)  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.ComponentModel.INotifyPropertyChanged>
- <xref:System.ComponentModel.BindingList%601>
- [Data binding in Windows Form](../../../docs/framework/winforms/windows-forms-data-binding.md)
- [Origini dati supportate da Windows Form](../../../docs/framework/winforms/data-sources-supported-by-windows-forms.md)
- [Data binding e Windows Forms](../../../docs/framework/winforms/data-binding-and-windows-forms.md)
