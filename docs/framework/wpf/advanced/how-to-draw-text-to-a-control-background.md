---
title: 'Procedura: Disegnare un testo sullo sfondo di un controllo'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], drawing text to backgrounds
- text [WPF], drawing to control backgrounds
- drawing [WPF], text to control backgrounds
- backgrounds [WPF], drawing text to
- typography [WPF], drawing text to control backgrounds
ms.assetid: 686d8fba-f61c-4974-a871-c635d67a7f69
ms.openlocfilehash: 9be4eb92021a62baaf6b43198587616d00cc265e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259254"
---
# <a name="how-to-draw-text-to-a-controls-background"></a>Procedura: Disegnare un testo sullo sfondo di un controllo
È possibile disegnare testo direttamente sullo sfondo di un controllo convertendo una stringa di testo a un <xref:System.Windows.Media.FormattedText> dell'oggetto e quindi disegnare l'oggetto per il controllo <xref:System.Windows.Media.DrawingContext>. È anche possibile usare questa tecnica per disegnare sullo sfondo di oggetti derivati da <xref:System.Windows.Controls.Panel>, ad esempio <xref:System.Windows.Controls.Canvas> e <xref:System.Windows.Controls.StackPanel>.  
  
 ![Controlli che visualizzano testo come sfondo](../../../../docs/framework/wpf/advanced/media/drawtext2background01.png "DrawText2Background01")  
Esempio di controlli con sfondi di testo personalizzati  
  
## <a name="example"></a>Esempio  
 Per disegnare sullo sfondo di un controllo, creare una nuova <xref:System.Windows.Media.DrawingBrush> dell'oggetto e disegnare il testo convertito dell'oggetto <xref:System.Windows.Media.DrawingContext>. Quindi, assegnare al nuovo <xref:System.Windows.Media.DrawingBrush> alla proprietà dello sfondo del controllo.  
  
 Esempio di codice seguente viene illustrato come creare un <xref:System.Windows.Media.FormattedText> dell'oggetto e disegnare lo sfondo di un <xref:System.Windows.Controls.Label> e <xref:System.Windows.Controls.Button> oggetto.  
  
 [!code-csharp[DrawTextToControlBackground#DrawTextToControlBackground1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawTextToControlBackground/CSHARP/Window1.xaml.cs#drawtexttocontrolbackground1)]  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Media.FormattedText>
- [Disegno di testo formattato](../../../../docs/framework/wpf/advanced/drawing-formatted-text.md)
