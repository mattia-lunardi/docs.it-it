---
title: "Procedura: Creare e utilizzare un'area di disegno"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Canvas
- Canvas control [WPF], creating
- Canvas control [WPF], using
ms.assetid: 420b9487-9a15-477c-9489-a22a4dec7779
ms.openlocfilehash: d2d56851de2444ce246750688df67ed5ba9adb9a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687479"
---
# <a name="how-to-create-and-use-a-canvas"></a>Procedura: Creare e utilizzare un'area di disegno
Questo esempio illustra come creare e usare un'istanza di <xref:System.Windows.Controls.Canvas>.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente posiziona in modo esplicito due <xref:System.Windows.Controls.TextBlock> elementi con il <xref:System.Windows.Controls.Canvas.SetTop%2A> e <xref:System.Windows.Controls.Canvas.SetLeft%2A> metodi di <xref:System.Windows.Controls.Canvas>. Nell'esempio viene inoltre assegnato un <xref:System.Windows.Controls.Control.Background%2A> colori della `LightSteelBlue` per il <xref:System.Windows.Controls.Canvas>.  
  
> [!NOTE]
>  Quando si usa [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] posizione <xref:System.Windows.Controls.TextBlock> gli elementi, utilizzare il <xref:System.Windows.Controls.Canvas.Top%2A> e <xref:System.Windows.Controls.Canvas.Left%2A> proprietà.  
  
 [!code-csharp[CanvasCode#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasCode/CSharp/Canvas_Code.cs#1)]
 [!code-vb[CanvasCode#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasCode/VisualBasic/canvas_vb.vb#1)]  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.TextBlock>
- <xref:System.Windows.Controls.Canvas.SetTop%2A>
- <xref:System.Windows.Controls.Canvas.SetLeft%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- [Cenni preliminari sugli elementi Panel](../../../../docs/framework/wpf/controls/panels-overview.md)
- [Procedure relative alle proprietà](../../../../docs/framework/wpf/controls/canvas-how-to-topics.md)
