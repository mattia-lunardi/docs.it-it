---
title: "Procedura: Eseguire l'associazione ai risultati di una query LINQ"
ms.date: 03/30/2017
helpviewer_keywords:
- running a LINQ query [WPF], bind to results
- binding to LINQ query results [WPF]
ms.assetid: ff2844d9-17ed-4ea6-aab1-5111af0bc684
ms.openlocfilehash: f39715cbfa0fe861f369ab313ac8fad11a347dbe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583068"
---
# <a name="how-to-bind-to-the-results-of-a-linq-query"></a>Procedura: Eseguire l'associazione ai risultati di una query LINQ
In questo esempio viene illustrato come eseguire una query LINQ e quindi eseguire l'associazione ai risultati.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente crea due caselle di riepilogo. Prima casella di riepilogo contiene tre voci di elenco.  
  
 [!code-xaml[LinqExample#UI](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml#ui)]  
  
 Selezione di un elemento dalla casella di riepilogo prima richiama il gestore eventi seguente. In questo esempio `Tasks` è una raccolta di `Task` oggetti. Il `Task` classe ha una proprietà denominata `Priority`. Questo gestore eventi viene eseguita una query LINQ che restituisce la raccolta di `Task` gli oggetti che hanno il valore di priorità selezionata e quindi imposta come il <xref:System.Windows.FrameworkElement.DataContext%2A>:  
  
 [!code-csharp[LinqExample#Using](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#using)]  
[!code-csharp[LinqExample#Tasks](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#tasks)]  
[!code-csharp[LinqExample#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LinqExample/CSharp/Window1.xaml.cs#handler)]  
  
 La seconda casella di riepilogo esegue l'associazione alla raccolta perché relativi <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> valore è impostato su `{Binding}`. Di conseguenza, viene visualizzato l'insieme restituito (in base il `myTaskTemplate` <xref:System.Windows.DataTemplate>).  
  
## <a name="see-also"></a>Vedere anche
- [Rendere i dati disponibili per l'associazione in XAML](../../../../docs/framework/wpf/data/how-to-make-data-available-for-binding-in-xaml.md)
- [Eseguire l'associazione a una raccolta e visualizzare informazioni in base alla selezione](../../../../docs/framework/wpf/data/how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [Novità di WPF versione 4.5](../../../../docs/framework/wpf/getting-started/whats-new.md)
- [Panoramica sul data binding](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [Procedure relative alle proprietà](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
