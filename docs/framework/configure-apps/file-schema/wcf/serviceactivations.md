---
title: <serviceActivations>
ms.date: 03/30/2017
ms.assetid: 97e665b6-1c51-410b-928a-9bb42c954ddb
ms.openlocfilehash: 7a091ecfbc0f4773ece620f93a9f21c219fcccb6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2019
ms.locfileid: "55256704"
---
# <a name="serviceactivations"></a>\<serviceActivations>
Elemento di configurazione che consente di aggiungere le impostazioni che definiscono le impostazioni di attivazione di servizi virtuali che eseguono il mapping ai tipi di servizio Windows Communication Foundation (WCF). In questo modo è possibile attivare servizi ospitati in WAS/IIS senza un file con estensione svc.  
  
 \<system.ServiceModel>  
\<serviceHostingEnvironment>  
\<serviceActivations>  
  
## <a name="syntax"></a>Sintassi  
  
```xml  
<serviceHostingEnvironment>
  <serviceActivations>
    <add factory="String"
         service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
 Nessuno.  
  
### <a name="child-elements"></a>Elementi figlio  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-serviceactivations.md)|Aggiunge un elemento di configurazione che specifica l'attivazione di un'applicazione di servizio.|  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[\<serviceHostingEnvironment>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|Definisce il tipo del quale l'ambiente host del servizio crea un'istanza per un determinato trasporto.|  
  
## <a name="remarks"></a>Note  
 Nell'esempio seguente viene illustrato come configurare le impostazioni di attivazione all'interno del file web.config.  
  
```xml  
<configuration>
  <system.serviceModel>
    <serviceHostingEnvironment>
      <serviceActivations>
        <add service="GreetingService" />
      </serviceActivations>
    </serviceHostingEnvironment>
  </system.serviceModel>
</configuration>
```  
  
 L'utilizzo di questa configurazione consente di attivare GreetingService senza usare un file con estensione svc.  
  
 Si noti che `<serviceHostingEnvironment>` è una configurazione a livello di applicazione. È necessario posizionare il file `web.config` contenente la configurazione nella radice dell'applicazione virtuale. Inoltre, `serviceHostingEnvironment` è una sezione ereditabile di machinetoApplication. Se si registra un servizio nella radice del computer, ogni servizio dell'applicazione erediterà tale servizio.  
  
 L'attivazione basata sulla configurazione supporta l'attivazione sul protocollo http e non http. A tale scopo sono necessarie le estensioni nell'indirizzo relativo, ovvero nei file con estensione svc, xoml o xamlx. È possibile eseguire il mapping di estensioni personalizzate ai provider di compilazione noti, consentendo in tal modo l'attivazione di servizi su qualsiasi estensione. In caso di conflitto, la sezione `<serviceActivations>` esegue l'override delle registrazioni nel file con estensione svc.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.ServiceModel.Configuration.ServiceActivationElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
