---
title: Risoluzione dei problemi generale per .NET Native
ms.date: 03/30/2017
ms.assetid: ee8c5e17-35ea-48a1-8767-83298caac1e8
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7717aba0fd3b3039dd77d301b10b044b5a044254
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596657"
---
# <a name="net-native-general-troubleshooting"></a>Risoluzione dei problemi generale per .NET Native
In questo argomento viene descritto come risolvere i problemi che potrebbero verificarsi durante lo sviluppo di app con [!INCLUDE[net_native](../../../includes/net-native-md.md)].  
  
-   **Problema:** La finestra di output di compilazione non viene aggiornata correttamente.  
  
     **Soluzione:** La finestra di output di compilazione non viene aggiornata finché non viene completata la compilazione. La compilazione può richiedere qualche minuto, quindi è possibile che si verifichi un ritardo nella visualizzazione degli aggiornamenti.  
  
-   **Problema:** Fase di compilazione delle vendite al dettaglio dell'app per ARM è aumentato.  
  
     **Soluzione:** Quando si distribuisce un'app nel dispositivo ARM, la [!INCLUDE[net_native](../../../includes/net-native-md.md)] infrastruttura viene richiamata. Questa compilazione esegue diverse ottimizzazioni, assicurando al tempo stesso il corretto funzionamento della semantica non statica, ad esempio la reflection. Inoltre, la parte di .NET Framework usata dall'app è collegata staticamente per assicurare prestazioni ottimizzate e deve essere compilata anch'essa in codice nativo. Ecco perché la compilazione richiede più tempo.  
  
     Tuttavia, i tempi di compilazione sono ancora compresi nell'intervallo di un minuto rispetto alla compilazione standard della maggior parte delle app in un computer di sviluppo standard.  In genere la semplice generazione di immagini native per .NET Framework in un computer di sviluppo standard richiede alcuni minuti.  Anche considerando tutte le ottimizzazioni per il miglioramento del codice generato e includendo .NET Framework, i tempi di compilazione dell'app corrispondono solitamente a un minuto o due.  
  
     Il processo di miglioramento delle prestazioni di compilazione è costante e viene eseguito analizzando la compilazione multithread e altre ottimizzazioni.  
  
-   **Problema:** Non si conosce se l'app è stata compilata usando [!INCLUDE[net_native](../../../includes/net-native-md.md)].  
  
     **Soluzione:** Se il [!INCLUDE[net_native](../../../includes/net-native-md.md)] compilatore viene richiamato, si noterà che è più tempi di compilazione e Gestione attività visualizzerà diversi [!INCLUDE[net_native](../../../includes/net-native-md.md)] processi dei componenti, ad esempio ILC.exe e nutc_driver.exe.  
  
     Dopo aver compilato correttamente il progetto con [!INCLUDE[net_native](../../../includes/net-native-md.md)], l'output è disponibile in obj\\*config*\ *arch*\\*nomeprogetto*.ilc\out.  I contenuti del pacchetto nativo finale sono disponibili in bin\\*arch*\\*config*\AppX. I contenuti del pacchetto nativo finale sono disponibili in \bin\\*arch*\\*config*\AppX se l'app è stata distribuita.  
  
-   **Problema:** L'app compilata in .NET Native sta generando eccezioni di runtime (in genere [MissingMetadataException](../../../docs/framework/net-native/missingmetadataexception-class-net-native.md) oppure [MissingRuntimeArtifactException](../../../docs/framework/net-native/missingruntimeartifactexception-class-net-native.md) eccezioni) che non sono state generate quando compilato senza. NET nativo.  
  
     **Soluzione:** Le eccezioni vengono generate perché .NET Native non ha fornito metadati o il codice di implementazione altrimenti disponibile attraverso la reflection. Per altre informazioni, vedere [Compilazione e .NET Native](../../../docs/framework/net-native/net-native-and-compilation.md). Per eliminare l'eccezione, si deve aggiungere una voce al proprio [file di direttive di runtime (rd.xml)](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md) in modo che la catena di strumenti di .NET Native possa rendere i metadati o il codice di implementazione disponibile in fase di esecuzione. Sono disponibili due strumenti di risoluzione dei problemi che genereranno la voce necessaria per l'aggiunta del file di direttive di runtime:  
  
    -   Lo [strumento di risoluzione dei problemi MissingMetadataException](https://dotnet.github.io/native/troubleshooter/type.html) per i tipi.  
  
    -   Lo [strumento di risoluzione dei problemi MissingMetadataException](https://dotnet.github.io/native/troubleshooter/method.html) per i metodi.  
  
     Per altre informazioni, vedere [Reflection e .NET Native](../../../docs/framework/net-native/reflection-and-net-native.md).  
  
## <a name="see-also"></a>Vedere anche
- [Migrazione dell'app di Windows Store a .NET Native](../../../docs/framework/net-native/migrating-your-windows-store-app-to-net-native.md)
