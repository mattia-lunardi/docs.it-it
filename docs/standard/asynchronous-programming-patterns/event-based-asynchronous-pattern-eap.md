---
title: Modello asincrono basato su eventi (EAP)
ms.date: 07/23/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- asynchronous calls
- asynchronous programming, design patterns
- asynchronous programming
ms.assetid: c6baed9f-2a25-4728-9a9a-53b7b14840cf
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 052773c615bcc4ddb5b735ae8164d44ed70bd935
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513490"
---
# <a name="event-based-asynchronous-pattern-eap"></a>Modello asincrono basato su eventi (EAP)

È possibile esporre funzionalità asincrone al codice client in molti modi. Il modello asincrono basato su eventi determina l'unico modo per la presentazione del comportamento asincrono da parte delle classi.  
  
> [!NOTE]
> A partire da .NET Framework 4, Task Parallel Library fornisce un nuovo modello di programmazione asincrona e parallela. Per altre informazioni, vedere [Task Parallel Library (TPL)](../parallel-programming/task-parallel-library-tpl.md) e [Task-based Asynchronous Pattern (TAP)](task-based-asynchronous-pattern-tap.md).
  
## <a name="in-this-section"></a>In questa sezione

 [Panoramica sul modello asincrono basato su eventi](event-based-asynchronous-pattern-overview.md)  
 Descrive il modo in cui il modello asincrono basato su eventi rende disponibili i vantaggi delle applicazioni multithread, nascondendo al tempo stesso molti dei problemi complessi correlati alla progettazione multithread.  
  
 [Implementazione del modello asincrono basato su eventi](implementing-the-event-based-asynchronous-pattern.md)  
 Descrive il modo standardizzato di creare un pacchetto di una classe con funzionalità asincrone.  
  
 [Suggerimenti per l'implementazione del modello asincrono basato su eventi](best-practices-for-implementing-the-event-based-asynchronous-pattern.md)  
 Descrive i requisiti per l'esposizione di funzionalità asincrone in base al modello asincrono basato su eventi.  
  
 [Quando implementare il modello asincrono basato su eventi](deciding-when-to-implement-the-event-based-asynchronous-pattern.md)  
 Descrive come stabilire quando occorre scegliere di implementare il modello asincrono basato su eventi anziché il modello <xref:System.IAsyncResult> rappresentato dal [modello di programmazione asincrona (APM)](asynchronous-programming-model-apm.md)
  
 [Procedura: Implementare un componente che supporta il modello asincrono basato su eventi](component-that-supports-the-event-based-asynchronous-pattern.md)  
 Spiega come creare un componente che implementa un modello asincrono basato su eventi. L'implementazione è eseguita mediante classi di helper dallo spazio dei nomi <xref:System.ComponentModel?displayProperty=nameWithType>, in modo da assicurare che il componente funzioni correttamente con qualsiasi modello di applicazione.  

 [Procedura: Implementare un client del modello asincrono basato su eventi](how-to-implement-a-client-of-the-event-based-asynchronous-pattern.md)  
 Spiega come creare un client che usa un componente che implementa un modello asincrono basato su eventi.
  
 [Procedura: Usare componenti che supportano il modello asincrono basato su eventi](how-to-use-components-that-support-the-event-based-asynchronous-pattern.md)  
 Descrive come usare un componente che supporta il modello asincrono basato su eventi.  
  
## <a name="reference"></a>Riferimenti

 <xref:System.ComponentModel.AsyncOperation>  
 Descrive la classe <xref:System.ComponentModel.AsyncOperation> e include collegamenti a tutti i membri corrispondenti.  
  
 <xref:System.ComponentModel.AsyncOperationManager>  
 Descrive la classe <xref:System.ComponentModel.AsyncOperationManager> e include collegamenti a tutti i membri corrispondenti.  
  
 <xref:System.ComponentModel.BackgroundWorker>  
 Descrive il componente <xref:System.ComponentModel.BackgroundWorker> e include collegamenti a tutti i membri corrispondenti.  
  
## <a name="related-sections"></a>Sezioni correlate

 [Task Parallel Library (TPL)](../parallel-programming/task-parallel-library-tpl.md)  
 Descrive un modello di programmazione delle operazioni asincrone e parallele.  
  
 [Threading](../../../docs/standard/threading/index.md)  
 Descrive le funzionalità di multithreading in .NET.  
  
## <a name="see-also"></a>Vedere anche

- [Suggerimenti per l'utilizzo del threading gestito](../threading/managed-threading-best-practices.md)
- [Eventi](../events/index.md)
- [Modelli di programmazione asincrona](index.md)
