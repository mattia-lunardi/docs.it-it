---
title: 'Procedura: Definire un rettangolo utilizzando RectangleGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rectangles
- rectangles [WPF], creating with RectangleGeometry class
ms.assetid: e40b8a8e-54b8-416b-a9f2-be6dca9fdf0b
ms.openlocfilehash: 9c57f1536065af0bca1f3752179547daa502c066
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511646"
---
# <a name="how-to-define-a-rectangle-using-a-rectanglegeometry"></a>Procedura: Definire un rettangolo utilizzando RectangleGeometry
In questo esempio viene descritto come utilizzare il <xref:System.Windows.Media.RectangleGeometry> classe per descrivere un rettangolo.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente viene illustrato come creare ed eseguire il rendering di un <xref:System.Windows.Media.RectangleGeometry>.  La posizione relativa e le dimensioni del rettangolo sono definite da un <xref:System.Windows.Rect> struttura. È la posizione relativa `50,50` e l'altezza e la larghezza sono entrambe `25` la creazione di un quadrato. L'interno del rettangolo viene disegnato con un <xref:System.Windows.Media.Brushes.LemonChiffon%2A> pennello e il relativo profilo viene disegnato con un <xref:System.Windows.Media.Brushes.Black%2A> tratto con uno spessore pari a `1`.  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRectangleGeometryExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmrectanglegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmrectanglegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmrectanglegeometryexample)]  
  
 ![Un oggetto RectangleGeometry](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-rectangle.gif "graphicsmm_rectangle")  
RectangleGeometry  
  
 Anche se in questo esempio viene utilizzato un <xref:System.Windows.Shapes.Path> elemento per il rendering le <xref:System.Windows.Media.RectangleGeometry>, sono disponibili molti altri modi per usare <xref:System.Windows.Media.RectangleGeometry> oggetti. Ad esempio, un <xref:System.Windows.Media.RectangleGeometry> può essere utilizzato per specificare il <xref:System.Windows.UIElement.Clip%2A> di un <xref:System.Windows.UIElement> o il <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> di un <xref:System.Windows.Media.GeometryDrawing>.  
  
 Le altre classi di geometrie semplici includono <xref:System.Windows.Media.LineGeometry> e <xref:System.Windows.Media.EllipseGeometry>. Questi oggetti Geometry, nonché quelle più complesse, è inoltre possibile creare utilizzando un <xref:System.Windows.Media.PathGeometry> o <xref:System.Windows.Media.StreamGeometry>.  
  
## <a name="see-also"></a>Vedere anche
- [Cenni preliminari sulle classi Geometry](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)
- [Creare una forma composta](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-composite-shape.md)
- [Creare una forma usando un oggetto PathGeometry](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-shape-by-using-a-pathgeometry.md)
