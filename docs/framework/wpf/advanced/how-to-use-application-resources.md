---
title: 'Procedura: Utilizzare le risorse delle applicazioni'
ms.date: 03/30/2017
helpviewer_keywords:
- application resources [WPF]
- resources [WPF], application resources
ms.assetid: 507ea937-5191-406b-8797-0a3d9f94156d
ms.openlocfilehash: acd172448ebdefd6395feec6ad50e1c9491d9e27
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733597"
---
# <a name="how-to-use-application-resources"></a>Procedura: Utilizzare le risorse delle applicazioni
In questo esempio viene illustrato come usare le risorse delle applicazioni.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente mostra un file di definizione dell'applicazione (ADF). Il file di definizione dell'applicazione definisce una sezione di risorse (un valore per il <xref:System.Windows.Application.Resources%2A> proprietà). Le risorse definite a livello di applicazione sono accessibili da tutte le altre pagine che fanno parte dell'applicazione. In questo caso, la risorsa è uno stile dichiarato. Poiché uno stile completo che include un modello di controllo può richiedere molto tempo, in questo esempio viene omesso il modello di controllo definito all'interno di <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> setter delle proprietà dello stile.  
  
 [!code-xaml[ResourcesApplication#PreTemplateResource](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ResourcesApplication/CS/app.xaml#pretemplateresource)]  
[!code-xaml[ResourcesApplication#PostTemplateResource](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ResourcesApplication/CS/app.xaml#posttemplateresource)]  
  
 L'esempio seguente mostra un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] pagina che fa riferimento alla risorsa a livello di applicazione definita nell'esempio precedente. La risorsa viene fatto riferimento tramite un [estensione di Markup StaticResource](../../../../docs/framework/wpf/advanced/staticresource-markup-extension.md) che specifica la chiave di risorsa univoco per la risorsa richiesta. Nella pagina corrente non è stata rilevata alcuna risorsa con chiave "GelButton", pertanto l'ambito di ricerca per la risorsa richiesta continua oltre la pagina corrente e nelle risorse definite a livello di applicazione.  
  
 [!code-xaml[ResourcesApplication#ConsumingPage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ResourcesApplication/CS/page1.xaml#consumingpage)]  
  
## <a name="see-also"></a>Vedere anche
- [Risorse XAML](../../../../docs/framework/wpf/advanced/xaml-resources.md)
- [Cenni preliminari sulla gestione di applicazioni](../../../../docs/framework/wpf/app-development/application-management-overview.md)
- [Procedure relative alle proprietà](../../../../docs/framework/wpf/advanced/resources-how-to-topics.md)
