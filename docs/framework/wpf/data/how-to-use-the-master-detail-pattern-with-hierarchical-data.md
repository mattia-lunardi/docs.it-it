---
title: 'Procedura: Utilizzare il modello Master-Details con dati gerarchici'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], Master-Detail data paradigm
- Master-Detail data paradigm
ms.assetid: 11429b9e-058d-4084-bfb6-2cf209c8ddf7
ms.openlocfilehash: 36eded28085aec3aaea1a2351ae3babc6ad6c700
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689640"
---
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-data"></a>Procedura: Utilizzare il modello Master-Details con dati gerarchici
In questo esempio viene illustrato come implementare lo scenario master-dettagli.  
  
## <a name="example"></a>Esempio  
 In questo esempio `LeagueList` è una raccolta di `Leagues`. Ciascuna `League` ha un `Name` e una raccolta di `Divisions`e ogni `Division` ha un nome e una raccolta di `Teams`. Ogni `Team` ha un nome.  
  
 [!code-xaml[MasterDetail#HowTo1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto1)]  
[!code-xaml[MasterDetail#HowTo2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto2)]  
  
 Lo screenshot seguente mostra l'esempio. Il `Divisions` <xref:System.Windows.Controls.ListBox> tiene automaticamente traccia delle selezioni nel `Leagues` <xref:System.Windows.Controls.ListBox> e visualizzare i dati corrispondenti. Il `Teams` <xref:System.Windows.Controls.ListBox> tiene traccia delle selezioni negli altri due <xref:System.Windows.Controls.ListBox> controlli.  
  
 ![Master&#45;esempio di detail](../../../../docs/framework/wpf/data/media/databindingmasterdetailsample.png "DataBindingMasterDetailSample")  
  
 I due aspetti da notare in questo esempio sono:  
  
1.  I tre <xref:System.Windows.Controls.ListBox> associare i controlli alla stessa origine. Impostare il <xref:System.Windows.Data.Binding.Path%2A> proprietà dell'associazione per specificare il livello di dati di cui si vuole il <xref:System.Windows.Controls.ListBox> da visualizzare.  
  
2.  È necessario impostare il <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> proprietà `true` nel <xref:System.Windows.Controls.ListBox> controlli di cui la selezione si esegue il monitoraggio. Impostazione di questa proprietà garantisce che l'elemento selezionato è sempre impostato come il <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>. In alternativa, se il <xref:System.Windows.Controls.ListBox> Ottiene i dati da un <xref:System.Windows.Data.CollectionViewSource>, selezione e la valuta viene sincronizzato automaticamente.  
  
 La tecnica è leggermente diversa quando si usa [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] dei dati. Per un esempio, vedere [usare il modello Master-Details con dati XML gerarchici](../../../../docs/framework/wpf/data/how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md).  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.HierarchicalDataTemplate>
- [Eseguire l'associazione a una raccolta e visualizzare informazioni in base alla selezione](../../../../docs/framework/wpf/data/how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [Panoramica sul data binding](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [Panoramica sui modelli di dati](../../../../docs/framework/wpf/data/data-templating-overview.md)
- [Procedure relative alle proprietà](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
