---
title: Archiviazione e lettura di dati negli Appunti (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Clipboard, storing data to (My.Computer.Clipboard)
- Clipboard, reading from (My.Computer.Clipboard)
- Clipboard
- My.Computer.Clipboard object, tasks
- data [Visual Basic], Clipboard
- reading data, from Clipboard
ms.assetid: f690119a-4378-4f7d-b20e-d9377ef49496
ms.openlocfilehash: c8f15ac33ae92a13159c2a95435ba3d2391ace8d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739206"
---
# <a name="storing-data-to-and-reading-from-the-clipboard-visual-basic"></a>Archiviazione e lettura di dati negli Appunti (Visual Basic)
Gli Appunti possono essere usati per archiviare i dati, ad esempio testo e immagini. Poiché gli Appunti sono condivisi tra tutti i processi attivi, possono essere usati per trasferire dati tra di essi. L'oggetto `My.Computer.Clipboard` consente di accedere facilmente agli Appunti per leggere e scrivere.  
  
## <a name="reading-from-the-clipboard"></a>Lettura dagli Appunti  
 Usare il metodo <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.GetText%2A> per leggere il testo negli Appunti. Il codice seguente legge il testo e lo visualizza in una finestra di messaggio. Per far funzionare l'esempio, gli Appunti devono contenere testo archiviato.  
  
 [!code-vb[VbVbcnMyClipboard#4](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_1.vb)]  
  
 Questo esempio di codice è disponibile anche come frammento di codice IntelliSense. Nello strumento di selezione dei frammenti di codice il frammento di codice si trova in **Applicazioni Windows Form > Appunti**. Per altre informazioni, vedere [Code Snippets](/visualstudio/ide/code-snippets) (Frammenti di codice).  
  
 Usare il metodo <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.GetImage%2A> per recuperare un'immagine dagli Appunti. Questo esempio verifica se è disponibile un'immagine negli Appunti prima di tentarne il recupero e assegnarlo a `PictureBox1`.  
  
 [!code-vb[VbResourceTasks#16](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_2.vb)]  
  
 Questo esempio di codice è disponibile anche come frammento di codice IntelliSense. Nello strumento di selezione dei frammenti di codice il frammento di codice si trova in **Applicazioni Windows Form > Appunti**. Per altre informazioni, vedere [Frammenti di codice](/visualstudio/ide/code-snippets).  
  
 Gli elementi inseriti negli Appunti verranno mantenuti anche dopo l'arresto dell'applicazione.  
  
## <a name="determining-the-type-of-file-stored-in-the-clipboard"></a>Determinazione del tipo di file archiviati negli Appunti  
 I dati contenuti negli Appunti potrebbero avere diverse forme, ad esempio testo, file audio o immagine. Per determinare il tipo di file negli Appunti, è possibile usare metodi quali <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsAudio%2A>, <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsFileDropList%2A>, <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsImage%2A> e <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsText%2A>. Il metodo <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.ContainsData%2A> può essere usato nel caso in cui si voglia controllare un formato personalizzato.  
  
 Usare la funzione `ContainsImage` per determinare se i dati contenuti negli Appunti costituiscono un'immagine. Il codice seguente consente di controllare se i dati costituiscono un'immagine e invia una segnalazione in merito.  
  
 [!code-vb[VbResourceTasks#13](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_3.vb)]  
  
## <a name="clearing-the-clipboard"></a>Cancellazione degli Appunti  
 Il metodo <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.Clear%2A> cancella il contenuto degli Appunti. Poiché gli Appunti sono condivisi da altri processi, la cancellazione può avere conseguenze su tali processi.  
  
 Nell'esempio di codice seguente viene illustrato come utilizzare il metodo `Clear`.  
  
 [!code-vb[VbVbcnMyClipboard#3](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_4.vb)]  
  
## <a name="writing-to-the-clipboard"></a>Scrittura negli Appunti  
 Usare il metodo <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetText%2A> per scrivere testo negli Appunti. Il codice seguente scrive la stringa "Questa è una stringa di prova" negli Appunti.  
  
 [!code-vb[VbVbcnMyClipboard#1](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_5.vb)]  
  
 Il metodo `SetText` può accettare un parametro di formato contenente un tipo di <xref:System.Windows.Forms.TextDataFormat>. Il codice seguente scrive la stringa "Questa è una stringa di prova" negli Appunti come testo RTF.  
  
 [!code-vb[VbVbcnMyClipboard#2](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_6.vb)]  
  
 Usare il metodo <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetData%2A> per scrivere dati negli Appunti. In questo esempio `DataObject` `dataChunk` viene scritto negli Appunti nel formato personalizzato `specialFormat`.  
  
 [!code-vb[VbVbcnMyClipboard#7](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_7.vb)]  
  
 Usare il metodo <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetAudio%2A> per scrivere dati audio negli Appunti. Questo esempio crea la matrice di byte `musicReader`, legge il file `cool.wav` al suo interno e lo scrive quindi negli Appunti.  
  
 [!code-vb[VbResourceTasks#5](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/storing-data-to-and-reading-from-the-clipboard_8.vb)]  
  
> [!IMPORTANT]
>  Dal momento che gli Appunti sono accessibili da altri utenti, non usarli per archiviare informazioni sensibili, ad esempio password o dati riservati.  
  
## <a name="see-also"></a>Vedere anche
- <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy>
- <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.GetAudioStream%2A>
- <xref:Microsoft.VisualBasic.MyServices.ClipboardProxy.SetDataObject%2A>
- [Procedura: Leggere dati oggetto in un file XML](../../../programming-guide/concepts/serialization/how-to-read-object-data-from-an-xml-file.md)
- [Procedura: Scrivere dati oggetto in un file XML](../../../programming-guide/concepts/serialization/how-to-write-object-data-to-an-xml-file.md)
