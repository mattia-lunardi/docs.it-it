---
title: 'Procedura: Creare un elemento Panel personalizzato'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Panel control [WPF]
- custom Panel elements [WPF]
ms.assetid: e0df4f1e-8c07-4e86-89a3-e22acfffdc2a
ms.openlocfilehash: 93d9ebacda8c753ab5a4446999e1aa86828a2b9e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54621932"
---
# <a name="how-to-create-a-custom-panel-element"></a>Procedura: Creare un elemento Panel personalizzato
## <a name="example"></a>Esempio  
 Questo esempio illustra come eseguire l'override del comportamento di layout predefinito del <xref:System.Windows.Controls.Panel> elemento e creare elementi di layout personalizzati che derivano dalla <xref:System.Windows.Controls.Panel>.  
  
 L'esempio definisce un oggetto personalizzato semplice <xref:System.Windows.Controls.Panel> elemento denominato `PlotPanel`, che posiziona gli elementi figlio in base a due hardcoded coordinate x e y-. In questo esempio `x` e `y` sono entrambe impostate su `50`; pertanto, tutti gli elementi figlio vengono posizionati nel percorso specificato su x e y assi.  
  
 Per implementare custom <xref:System.Windows.Controls.Panel> comportamenti predefiniti, nell'esempio viene usato il <xref:System.Windows.FrameworkElement.MeasureOverride%2A> e <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> metodi. Ogni metodo restituisce il <xref:System.Windows.Size> i dati necessari per posizionare e il rendering degli elementi figlio.  
  
 [!code-cpp[PlotPanel#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/PlotPanel/CPP/PlotPanel.cpp#1)]
 [!code-csharp[PlotPanel#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PlotPanel/CSharp/PlotPanel.cs#1)]
 [!code-vb[PlotPanel#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PlotPanel/VisualBasic/PlotPanel.vb#1)]  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Controls.Panel>
- [Cenni preliminari sugli elementi Panel](../../../../docs/framework/wpf/controls/panels-overview.md)
- [Creare un contenuto-Wrapping Panel Sample personalizzato](https://go.microsoft.com/fwlink/?LinkID=159979)
