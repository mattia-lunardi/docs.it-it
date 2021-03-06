---
title: Analizzatori basati su Roslyn - .NET
description: Informazioni sugli analizzatori basati su Roslyn che consentono di individuare problemi e suggeriscono correzioni per tali problemi.
author: billwagner
ms.author: billwagner
ms.date: 01/24/2018
ms.technology: dotnet-standard
ms.openlocfilehash: 226482d1d385078811f2b1c5ee138e24287a785e
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2018
ms.locfileid: "53154333"
---
# <a name="the-roslyn-based-analyzers"></a>Analizzatori basati su Roslyn

Gli analizzatori basati su Roslyn usano .NET Compiler SDK (API Roslyn) per analizzare il codice sorgente del progetto per individuare i problemi e suggerire le correzioni. Analizzatori diversi cercano classi di problemi differenti, ad esempio procedure destinate probabilmente a causare bug, problematiche di sicurezza e compatibilità delle API.

Gli analizzatori basati su Roslyn operano sia in modo interattivo che durante le compilazioni. L'analizzatore propone indicazioni diverse per le compilazioni in Visual Studio o dalla riga di comando.

Durante la modifica di codice in Visual Studio, gli analizzatori vengono eseguiti mentre si apportano modifiche, intercettando i possibili problemi non appena si crea codice potenzialmente problematico. Gli eventuali problemi vengono evidenziati con una sottolineatura a zigzag. Visual Studio visualizza una lampadina e facendo clic su di essa l'analizzatore propone suggerimenti per le possibili correzioni per il problema. Quando si compila il progetto, in Visual Studio o dalla riga di comando, viene analizzato tutto il codice sorgente e l'analizzatore fornisce un elenco completo dei potenziali problemi. Nella figura seguente viene mostrato un esempio.

![Problemi segnalati dall'analizzatore del framework](./media/framework-analyzers-2.png)

Gli analizzatori basati su Roslyn segnalano i potenziali problemi come errori, avvisi o informazioni in base alla gravità del problema.

Gli analizzatori basati su Roslyn vengono installati come pacchetti NuGet nel progetto. Gli analizzatori configurati e le eventuali impostazioni per ogni analizzatore vengono ripristinati ed eseguiti nel computer di qualsiasi sviluppatore per il progetto.

> [!NOTE]
> L'esperienza utente per gli analizzatori basati su Roslyn è diversa rispetto a quella delle librerie di analisi del codice come le versioni precedenti di FxCop e gli strumenti di analisi della sicurezza.  Non è necessario eseguire in modo esplicito gli analizzatori basati su Roslyn. Non occorre usare le voci di menu "Esegui analisi del codice" nel menu "Analizza" in Visual Studio. Gli analizzatori basati su Roslyn vengono eseguiti in modo asincrono durante il lavoro. 

## <a name="more-information-on-specific-analyzers"></a>Altre informazioni su analizzatori specifici

In questa sezione vengono presentati gli analizzatori seguenti:

* [API Analyzer](api-analyzer.md): questo analizzatore esamina il codice per individuare potenziali rischi per la compatibilità o l'uso di API deprecate.    
* [Framework Analyzer](framework-analyzer.md): questo analizzatore esamina il codice per assicurarsi che segua le linee guida per le applicazioni .NET Framework. Queste regole includono numerose raccomandazioni basate sulla sicurezza.
* [.NET Portability Analyzer](portability-analyzer.md): questo analizzatore esamina il codice per valutare la quantità di lavoro necessario per rendere l'applicazione compatibile con altri profili e implementazioni di .NET, tra cui .NET Core, .NET Standard, UWP e Xamarin per iOS, Android e Mac. 
