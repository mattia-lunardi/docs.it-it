---
title: 'Procedura: creare un effetto di attivazione utilizzando gli eventi'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors of elements [WPF], changing
- rollover effect [WPF]
- element colors [WPF], changing
ms.assetid: 3b20d028-6f1c-4b25-95d2-fa68cefbdb4c
ms.openlocfilehash: d458d87586614093b35fcd73969dea04fe620351
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543010"
---
# <a name="how-to-create-a-rollover-effect-using-events"></a>Procedura: creare un effetto di attivazione utilizzando gli eventi
In questo esempio viene illustrato come modificare il colore di un elemento quando il puntatore del mouse entra o esce dall'area occupata dall'elemento.  
  
 In questo esempio è costituito un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file e un file code-behind.  
  
> [!NOTE]
>  Questo esempio viene illustrato come utilizzare gli eventi, ma il metodo consigliato per ottenere lo stesso effetto consiste nell'utilizzare un <xref:System.Windows.Trigger> in uno stile. Per altre informazioni, vedere [Applicazione di stili e modelli](../../../../docs/framework/wpf/controls/styling-and-templating.md).  
  
## <a name="example"></a>Esempio  
 Le operazioni seguenti [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] crea l'interfaccia utente, che è costituito da <xref:System.Windows.Controls.Border> intorno un <xref:System.Windows.Controls.TextBlock>e allega il <xref:System.Windows.Input.Mouse.MouseEnter> e <xref:System.Windows.UIElement.MouseLeave> gestori eventi per il <xref:System.Windows.Controls.Border>.  
  
 [!code-xaml[mouseenterMouseleave#MouseEnterLeaveSampleXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/mouseenterMouseleave/CSharp/Window1.xaml#mouseenterleavesamplexaml)]  
  
 Il codice seguente crea il <xref:System.Windows.UIElement.MouseEnter> e <xref:System.Windows.UIElement.MouseLeave> gestori eventi.  Quando il puntatore del mouse entra nell'area di <xref:System.Windows.Controls.Border>, lo sfondo del <xref:System.Windows.Controls.Border> diventa rosso.  Quando il puntatore del mouse esce dall'area di <xref:System.Windows.Controls.Border>, lo sfondo del <xref:System.Windows.Controls.Border> ritorna bianco.  
  
 [!code-csharp[mouseenterMouseleave#MouseEnterLeaveSampleEventHandlers](../../../../samples/snippets/csharp/VS_Snippets_Wpf/mouseenterMouseleave/CSharp/Window1.xaml.cs#mouseenterleavesampleeventhandlers)]
 [!code-vb[mouseenterMouseleave#MouseEnterLeaveSampleEventHandlers](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/mouseenterMouseleave/VisualBasic/Window1.xaml.vb#mouseenterleavesampleeventhandlers)]
