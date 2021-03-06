---
title: 'Procedura: Usare Svcutil.exe per convalidare il codice del servizio compilato'
ms.date: 03/30/2017
ms.assetid: d0d820fb-41c2-45b8-8f22-0fa5aeebbbaa
ms.openlocfilehash: a06cf57fce883753af4686b294396d6d6da73a13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54531928"
---
# <a name="how-to-use-svcutilexe-to-validate-compiled-service-code"></a>Procedura: Usare Svcutil.exe per convalidare il codice del servizio compilato
È possibile usare la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) per rilevare errori in configurazioni e le implementazioni del servizio senza ospitare il servizio.  
  
### <a name="to-validate-a-service"></a>Per convalidare un servizio  
  
1.  Compilare il servizio in un file eseguibile e in uno o più assembly dipendenti.  
  
2.  Aprire un prompt dei comandi SDK.  
  
3.  Al prompt dei comandi, avviare lo strumento Svcutil.exe usando il formato seguente. Per altre informazioni sui vari parametri, vedere la sezione convalida del servizio di [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) argomento.  
  
    ```  
    svcutil.exe /validate /serviceName:<serviceConfigName>  <assemblyPath>*  
    ```  
  
     È necessario usare l'opzione `/serviceName` per indicare il nome di configurazione del servizio che si desidera convalidare.  
  
     L'argomento `assemblyPath` specifica il percorso del file eseguibile per il servizio e uno o più assembly che contengono i tipi di servizio da convalidare. L'assembly eseguibile deve avere un file di configurazione associato per fornire la configurazione del servizio. È possibile usare caratteri jolly della riga di comando standard per fornire più assembly.  
  
## <a name="example"></a>Esempio  
 Il comando seguente implementa il servizio myServiceName nel file eseguibile myServiceHost.exe.  Il file di configurazione per il servizio (myServiceHost.exe.config) viene automaticamente caricato.  
  
```  
svcutil /validate /serviceName:myServiceName myServiceHost.exe  
```  
  
## <a name="see-also"></a>Vedere anche
- [Strumento ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
