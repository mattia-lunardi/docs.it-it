---
title: <pnrpPeerResolver>
ms.date: 03/30/2017
ms.assetid: c1b34f3b-68e5-4911-a367-de49fb61dbc6
ms.openlocfilehash: f98c358cc9891e9d7223d280fc8e50c19aad9759
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260651"
---
# <a name="pnrppeerresolver"></a>\<pnrpPeerResolver>
Specifica l'uso di PNRP (Peer Name Resolution Protocol) come resolver. Questo elemento è facoltativo perché PNRP è il resolver predefinito.  
  
 \<system.serviceModel>  
\<le associazioni >  
\<customBinding>  
\<binding>  
\<pnrpResolver>  
  
## <a name="syntax"></a>Sintassi  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
  
|Attributo|Descrizione|  
|---------------|-----------------|  
|resolverType|Stringa che specifica il resolver da usare. L'attributo è facoltativo. Se non è impostato o se è impostato su una stringa vuota, viene usato PNRP.|  
  
### <a name="child-elements"></a>Elementi figlio  
 nessuno  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[\<binding>](../../../../../docs/framework/misc/binding.md)|Definisce tutte le funzionalità di associazione dell'associazione personalizzata.|  
  
## <a name="example"></a>Esempio  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement>
- <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [Associazioni](../../../../../docs/framework/wcf/bindings.md)
- [Estensione delle associazioni](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Associazioni personalizzate](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [Resolver del peer](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
