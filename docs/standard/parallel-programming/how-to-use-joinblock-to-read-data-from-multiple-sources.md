---
title: 'Procedura: usare JoinBlock per leggere dati da più origini'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Task Parallel Library, dataflows
- TPL dataflow library, joining blocks in
- dataflow blocks, joining in TPL
ms.assetid: e9c1ada4-ac57-4704-87cb-2f5117f8151d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0031e352fea845ca4831b4df3a67c9cc6b67e876
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222285"
---
# <a name="how-to-use-joinblock-to-read-data-from-multiple-sources"></a>Procedura: usare JoinBlock per leggere dati da più origini
In questo documento viene spiegato come utilizzare la classe <xref:System.Threading.Tasks.Dataflow.JoinBlock%602> per eseguire un'operazione quando i dati sono disponibili da più origini. Viene inoltre illustrato come utilizzare la modalità non greedy per consentire la condivisione in modo più efficiente di un'origine dati da parte di più blocchi join.

[!INCLUDE [tpl-install-instructions](../../../includes/tpl-install-instructions.md)]

## <a name="example"></a>Esempio  
 Nell'esempio seguente vengono definiti tre tipi di risorsa, `NetworkResource`, `FileResource` e `MemoryResource` e vengono eseguite operazioni quando queste diventano disponibili. Per questo esempio è richiesta una coppia `NetworkResource` e `MemoryResource` per eseguire la prima operazione e una coppia `FileResource` e `MemoryResource` per eseguire la seconda. Per consentire l'esecuzione di queste operazioni quando tutte le risorse necessarie sono disponibili, nell'esempio viene utilizzata la classe <xref:System.Threading.Tasks.Dataflow.JoinBlock%602>. Quando tramite un oggetto <xref:System.Threading.Tasks.Dataflow.JoinBlock%602> vengono ricevuti dati da tutte le origini, questi dati vengono propagati alla relativa destinazione, che in questo esempio è un oggetto <xref:System.Threading.Tasks.Dataflow.ActionBlock%601>. La lettura da parte di entrambi gli oggetti <xref:System.Threading.Tasks.Dataflow.JoinBlock%602> viene eseguita da un pool condiviso di oggetti `MemoryResource`.  
  
 [!code-csharp[TPLDataflow_NonGreedyJoin#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_nongreedyjoin/cs/nongreedyjoin.cs#1)]
 [!code-vb[TPLDataflow_NonGreedyJoin#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_nongreedyjoin/vb/nongreedyjoin.vb#1)]  
  
 Per consentire un utilizzo efficiente del pool condiviso di oggetti `MemoryResource`, in questo esempio viene specificato un oggetto <xref:System.Threading.Tasks.Dataflow.GroupingDataflowBlockOptions> con la proprietà <xref:System.Threading.Tasks.Dataflow.GroupingDataflowBlockOptions.Greedy%2A> impostata su `False` per creare oggetti <xref:System.Threading.Tasks.Dataflow.JoinBlock%602> utilizzati in modalità non greedy. In un blocco join non greedy tutti i messaggi in ingresso vengono posticipati finché non ne è disponibile uno da ogni origine. Se uno dei messaggi posposti viene accettato da un altro blocco, tramite il blocco join viene riavviato il processo. La modalità non greedy consente ai blocchi join in cui vengono condivisi uno o più blocchi di origine di proseguire il lavoro mentre i dati vengono attesi dagli altri blocchi. In questo esempio, se un oggetto `MemoryResource` viene aggiunto al pool `memoryResources`, il primo blocco join utilizzato per ricevere la seconda origine dati può continuare. Se in questo esempio venisse utilizzata la modalità greedy, vale a dire l'impostazione predefinita, un blocco join potrebbe accettare l'oggetto `MemoryResource` e attendere che la seconda risorsa diventi disponibile. Tuttavia, se nell'altro blocco join è presente la seconda origine dati disponibile, non è possibile continuare perché l'oggetto `MemoryResource` è stato accettato dall'altro blocco join.  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 Copiare il codice di esempio e incollarlo in un progetto di Visual Studio oppure incollarlo in un file denominato `DataflowNonGreedyJoin.cs` (`DataflowNonGreedyJoin.vb` per Visual Basic) e quindi eseguire il comando riportato di seguito in una finestra del prompt dei comandi per gli sviluppatori per Visual Studio.  
  
 Visual C#  
  
 **csc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowNonGreedyJoin.cs**  
  
 Visual Basic  
  
 **vbc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowNonGreedyJoin.vb**  
  
## <a name="robust-programming"></a>Programmazione efficiente  
 L'utilizzo di join non greedy può inoltre aiutare a impedire un deadlock nell'applicazione. In un'applicazione software si verifica un *deadlock* quando due o più processi bloccano ognuno una risorsa e attendono entrambi che un altro processo rilasci altre risorse. Si consideri un'applicazione in cui sono definiti due oggetti <xref:System.Threading.Tasks.Dataflow.JoinBlock%602>. I dati dei due blocchi di origine condivisi possono essere letti da entrambi gli oggetti. In modalità greedy, se la prima origine viene letta dal primo blocco e la seconda origine dal secondo blocco, si potrebbe verificare un deadlock dell'applicazione poiché entrambi i blocchi join sono in attesa del completamento dell'altro per liberare la relativa risorsa. In modalità non greedy, la lettura dalle relative origini da parte di ogni blocco join viene eseguita solo quando tutti i dati sono disponibili e, di conseguenza, il rischio di deadlock è eliminato.  
  
## <a name="see-also"></a>Vedere anche

- [Flusso di dati](../../../docs/standard/parallel-programming/dataflow-task-parallel-library.md)
