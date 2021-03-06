---
title: 'Procedura: Analizzare percorsi di file in Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- file names [Visual Basic], parsing [Visual Basic]
- parsing, file paths [Visual Basic]
ms.assetid: c1bd99c9-8160-456a-b5ab-60a49139b923
ms.openlocfilehash: 2b31dedbdd33ddfb3c15863a45b93148fd722faa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707752"
---
# <a name="how-to-parse-file-paths-in-visual-basic"></a>Procedura: Analizzare percorsi di file in Visual Basic
L'oggetto <xref:Microsoft.VisualBasic.FileIO.FileSystem> offre una serie di metodi utili per l'analisi dei percorsi di file.  
  
-   Il metodo <xref:Microsoft.VisualBasic.FileIO.FileSystem.CombinePath%2A> accetta due percorsi e restituisce un percorso combinato correttamente formattato.  
  
-   Il metodo <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetParentPath%2A> restituisce il percorso assoluto dell'elemento padre del percorso specificato.  
  
-   Il metodo <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFileInfo%2A> restituisce un oggetto <xref:System.IO.FileInfo> su cui è possibile eseguire query per determinare le proprietà del file, ad esempio il nome e il percorso.  
  
 Non basarsi sull'estensione del nome del file per prendere decisioni in merito al relativo contenuto. È possibile ad esempio che il file Form1.vb non sia un file di origine di Visual Basic.  
  
### <a name="to-determine-a-files-name-and-path"></a>Per determinare il nome e il percorso di un file  
  
-   Usare le proprietà <xref:System.IO.FileInfo.DirectoryName%2A> e <xref:System.IO.FileInfo.Name%2A> dell'oggetto <xref:System.IO.FileInfo> per determinare il nome e il percorso di un file. In questo esempio il nome e il percorso vengono determinati e quindi visualizzati.  
  
     [!code-vb[VbVbcnMyFileSystem#54](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-parse-file-paths_1.vb)]  
  
### <a name="to-combine-a-files-name-and-directory-to-create-the-full-path"></a>Per combinare il nome e la directory di un file per creare il percorso completo  
  
-   Usare il metodo `CombinePath` , specificando la directory e il nome. In questo esempio vengono combinate le stringhe `folderPath` e `fileName` create nell'esempio precedente e viene visualizzato il risultato.  
  
     [!code-vb[VbVbcnMyFileSystem#55](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-parse-file-paths_2.vb)]  
  
## <a name="see-also"></a>Vedere anche
- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CombinePath%2A>
- <xref:System.IO.FileInfo>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFileInfo%2A>
- [Procedura: Ottenere la raccolta di file di una directory](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-get-the-collection-of-files-in-a-directory.md)
