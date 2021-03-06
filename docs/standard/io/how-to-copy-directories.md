---
title: 'Procedura: Copiare le directory'
ms.date: 12/27/2018
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- directory copying
- I/O [.NET Framework], copying directories
- subdirectory copying
- copying directories
- directories [.NET Framework], copying
ms.assetid: 5a969765-e5f8-4b4e-977e-90e2b0a1fe3c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 57e2b61fb8fef37234dc10885752f92e5f9b1330
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671070"
---
# <a name="how-to-copy-directories"></a>Procedura: Copiare le directory
Questo argomento illustra come usare le classi di I/O per copiare in modalità sincrona il contenuto di una directory in un'altra posizione. 

Per un esempio di copia di file asincrona, vedere [I/O di file asincrono](../../../docs/standard/io/asynchronous-file-i-o.md). 

In questo esempio le sottodirectory vengono copiate impostando l'elemento `copySubDirs` del metodo `DirectoryCopy` su `true`. Il metodo `DirectoryCopy` copia le sottodirectory in modo ricorsivo chiamando se stesso in ogni sottodirectory finché non ci sono più sottodirectory da copiare.  
  
## <a name="example"></a>Esempio  
 [!code-csharp[System.IO.Directory_Copy#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.IO.Directory_Copy/cs/program.cs#1)]
 [!code-vb[System.IO.Directory_Copy#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.IO.Directory_Copy/vb/Program.vb#1)]  
  
## <a name="see-also"></a>Vedere anche

- <xref:System.IO.FileInfo>
- <xref:System.IO.DirectoryInfo>
- <xref:System.IO.FileStream>
- [I/O di file e di flussi](../../../docs/standard/io/index.md)
- [Attività di I/O comuni](../../../docs/standard/io/common-i-o-tasks.md)
- [I/O di file asincrono](../../../docs/standard/io/asynchronous-file-i-o.md)