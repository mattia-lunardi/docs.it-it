---
title: "Procedura: Eseguire l'associazione a una raccolta e visualizzare informazioni in base alla selezione"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data collections [WPF], selecting data for views
- data binding [WPF], creating views of data collections
- data binding [WPF], selecting data for views
- data binding [WPF], binding to collections
ms.assetid: 952a7d76-dd29-49e5-86f5-32c4530e70eb
ms.openlocfilehash: 549f4e7af1a9aa623c7f8ff12b528f771a8ff806
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504776"
---
# <a name="how-to-bind-to-a-collection-and-display-information-based-on-selection"></a>Procedura: Eseguire l'associazione a una raccolta e visualizzare informazioni in base alla selezione
In uno scenario master-dettagli semplice, è necessario con associazione a dati <xref:System.Windows.Controls.ItemsControl> , ad esempio un <xref:System.Windows.Controls.ListBox>. È basato sulla selezione dell'utente, visualizzare altre informazioni sull'elemento selezionato. In questo esempio viene illustrato come implementare questo scenario.  
  
## <a name="example"></a>Esempio  
 In questo esempio `People` è un <xref:System.Collections.ObjectModel.ObservableCollection%601> di `Person` classi. Ciò `Person` classe contiene tre proprietà: `FirstName`, `LastName`, e `HomeTown`, tutti di tipo `string`.  
  
 [!code-xaml[CollectionBinding#Source](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#source)]  
[!code-xaml[CollectionBinding#UI](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#ui)]  
  
 Il <xref:System.Windows.Controls.ContentControl> utilizza il seguente <xref:System.Windows.DataTemplate> che definisce come le informazioni di un `Person` viene presentato:  
  
 [!code-xaml[CollectionBinding#DetailTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#detailtemplate)]  
  
 Di seguito è riportato uno screenshot del risultato dell'esempio. Il <xref:System.Windows.Controls.ContentControl> Mostra le altre proprietà della persona selezionata.  
  
 ![Associazione a una raccolta](../../../../docs/framework/wpf/data/media/databinding-collectionbindingsample.png "DataBinding_CollectionBindingSample")  
  
 I due aspetti da notare in questo esempio sono:  
  
1.  Il <xref:System.Windows.Controls.ListBox> e il <xref:System.Windows.Controls.ContentControl> associare alla stessa origine. Il <xref:System.Windows.Data.Binding.Path%2A> le proprietà di entrambe le associazioni non vengono specificate perché entrambi i controlli vengono associati all'intero oggetto collection.  
  
2.  È necessario impostare il <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> proprietà `true` per il corretto funzionamento. Impostazione di questa proprietà garantisce che l'elemento selezionato è sempre impostato come il <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>. In alternativa, se il <xref:System.Windows.Controls.ListBox> Ottiene i dati da un <xref:System.Windows.Data.CollectionViewSource>, selezione e la valuta viene sincronizzato automaticamente.  
  
 Si noti che il `Person` classe esegue l'override di `ToString` metodo modo seguente. Per impostazione predefinita, il <xref:System.Windows.Controls.ListBox> chiamate `ToString` e visualizza una rappresentazione di stringa di ogni oggetto nella raccolta associata. Ecco perché ogni `Person` appare come un nome nel <xref:System.Windows.Controls.ListBox>.  
  
 [!code-csharp[CollectionBinding#ToString](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Data.cs#tostring)]
 [!code-vb[CollectionBinding#ToString](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionBinding/VisualBasic/Person.vb#tostring)]  
  
## <a name="see-also"></a>Vedere anche
- [Usare il modello Master-Details con dati gerarchici](../../../../docs/framework/wpf/data/how-to-use-the-master-detail-pattern-with-hierarchical-data.md)
- [Usare il modello Master-Details con dati XML gerarchici](../../../../docs/framework/wpf/data/how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md)
- [Panoramica sul data binding](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [Panoramica sui modelli di dati](../../../../docs/framework/wpf/data/data-templating-overview.md)
- [Procedure relative alle proprietà](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
