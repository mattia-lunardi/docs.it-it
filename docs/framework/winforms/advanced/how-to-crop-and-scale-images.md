---
title: 'Procedura: Ritagliare e adattare immagini'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], cropping
- images [Windows Forms], scaling
ms.assetid: 053e3360-bca0-4b25-9afa-0e77a6f17b03
ms.openlocfilehash: 1f6d721edc4f889c2da8ece63f262c7fb55192bd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707700"
---
# <a name="how-to-crop-and-scale-images"></a>Procedura: Ritagliare e adattare immagini
Il <xref:System.Drawing.Graphics> classe sono disponibili numerosi <xref:System.Drawing.Graphics.DrawImage%2A> metodi, alcuni dei quali sono i parametri rettangolo di origine e di destinazione che è possibile usare per ritagliare e adattare immagini.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente si costruisce un <xref:System.Drawing.Image> oggetto dal file di disco Apple. Il codice disegna l'immagine di apple intero nelle dimensioni originali. Il codice chiama quindi il <xref:System.Drawing.Graphics.DrawImage%2A> metodo di un <xref:System.Drawing.Graphics> oggetto su cui disegnare una parte dell'immagine di apple in un rettangolo di destinazione che è maggiore dell'immagine originale.  
  
 Il <xref:System.Drawing.Graphics.DrawImage%2A> metodo determina quale parte di apple per disegnare esaminando il rettangolo di origine, specificata dalla terza, quarta, quinto e sesto argomento. In questo caso, viene ritagliata apple al 75% della larghezza e al 75% della relativa altezza.  
  
 Il <xref:System.Drawing.Graphics.DrawImage%2A> metodo determina la posizione in cui disegnare il mela e quali dimensioni ritagliata esaminando il rettangolo di destinazione, che è specificato dal secondo argomento. In questo caso, il rettangolo di destinazione è pari al 30% più ampio e il 30% più alto rispetto all'immagine originale.  
  
 La figura seguente mostra l'originale e l'immagine adattata, ritagliata.  
  
 ![Crop & Scale](../../../../docs/framework/winforms/advanced/media/cscropscale1.png "csCropScale1")  
  
 [!code-csharp[System.Drawing.WorkingWithImages#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.WorkingWithImages#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio precedente è progettato per l'uso con Windows Form e richiede <xref:System.Windows.Forms.PaintEventArgs> `e`, un parametro del gestore eventi <xref:System.Windows.Forms.Control.Paint>. Assicurarsi di sostituire `Apple.gif` con un nome file di immagine e il percorso che sono validi per il sistema.  
  
## <a name="see-also"></a>Vedere anche
- [Immagini, bitmap e metafile](../../../../docs/framework/winforms/advanced/images-bitmaps-and-metafiles.md)
- [Utilizzo di immagini, bitmap, icone e metafile](../../../../docs/framework/winforms/advanced/working-with-images-bitmaps-icons-and-metafiles.md)
