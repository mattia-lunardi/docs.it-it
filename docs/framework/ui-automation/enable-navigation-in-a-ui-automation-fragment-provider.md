---
title: Consentire la navigazione in un provider di frammenti di automazione interfaccia utente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UI Automation, enabling navigation in provider
- navigation, enabling in UI Automation provider
ms.assetid: 3cb6092a-58c9-4ca0-84a5-0e54d5d00a0d
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: b920fbd118dd3757976a0fc48c42a0bb6dd97c6b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495223"
---
# <a name="enable-navigation-in-a-ui-automation-fragment-provider"></a>Consentire la navigazione in un provider di frammenti di automazione interfaccia utente
> [!NOTE]
>  Questa documentazione è destinata agli sviluppatori di .NET Framework che vogliono usare le classi gestite di [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] definite nello spazio dei nomi <xref:System.Windows.Automation>. Per informazioni aggiornate sulle [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], vedere [Windows Automation API: Automazione interfaccia utente](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Questo argomento contiene codice di esempio che illustra come abilitare la navigazione in un provider di automazione interfaccia utente per un elemento che si trova all'interno di un frammento.  
  
## <a name="example"></a>Esempio  
 L'esempio di codice seguente implementa <xref:System.Windows.Automation.Provider.IRawElementProviderFragment.Navigate%2A> per un elemento dell'elenco all'interno di un elenco. L'elemento padre è l'elemento casella di riepilogo e gli elementi di pari livello sono altri elementi nella raccolta di elenchi. Il metodo restituisce `null` (`Nothing` in Visual Basic) per le istruzioni che non sono valide; in questo caso, <xref:System.Windows.Automation.Provider.NavigateDirection.FirstChild> e <xref:System.Windows.Automation.Provider.NavigateDirection.LastChild>in quanto l'elemento non ha figli.  
  
 [!code-csharp[UIAFragmentProvider_snip#103](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAFragmentProvider_snip/CSharp/ListItemFragment.cs#103)]
 [!code-vb[UIAFragmentProvider_snip#103](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAFragmentProvider_snip/VisualBasic/ListItemFragment.vb#103)]  
  
## <a name="see-also"></a>Vedere anche
- [Panoramica dei provider di automazione interfaccia utente](../../../docs/framework/ui-automation/ui-automation-providers-overview.md)
- [Implementazione del provider di automazione interfaccia utente lato server](../../../docs/framework/ui-automation/server-side-ui-automation-provider-implementation.md)
