---
title: Interfaccia ICLRMetaHostPolicy
ms.date: 03/30/2017
api_name:
- ICLRMetaHostPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHostPolicy
helpviewer_keywords:
- ICLRMetaHostPolicy interface [.NET Framework hosting]
ms.assetid: 1bdeccb6-0698-4c97-ad69-eae2b69e59f1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 46576552db6e3c9aa06646b260e74cb4b7890d9d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54559229"
---
# <a name="iclrmetahostpolicy-interface"></a>Interfaccia ICLRMetaHostPolicy
Fornisce il [GetRequestedRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md) metodo, che restituisce un puntatore a un'interfaccia di runtime (CLR) di linguaggio comune basata su criteri, gestito al file di configurazione, versione e assembly.  
  
## <a name="methods"></a>Metodi  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[Metodo GetRequestedRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md)|Fornisce un'interfaccia CLR preferita basata su criteri, gestito al file di configurazione, versione e assembly.|  
  
## <a name="remarks"></a>Note  
 È possibile ottenere un riferimento a questa interfaccia mediante la chiamata di [CLRCreateInstance](../../../../docs/framework/unmanaged-api/hosting/clrcreateinstance-function.md) funzionano come illustrato nel codice seguente:  
  
```  
ICLRMetaHostPolicy *pMetaHostPolicy = NULL;  
HRESULT hr = CLRCreateInstance(CLSID_CLRMetaHostPolicy,  
                   IID_ICLRMetaHostPolicy, (LPVOID*)&pMetaHostPolicy);  
```  
  
> [!NOTE]
>  Questa interfaccia non effettivamente caricare o attivare il CLR, ma semplicemente restituisce la versione CLR preferita in base alle versioni disponibili che sono installate o caricate.  
  
 Il [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)] API di hosting consente di consolidare i criteri in modo che gli host grazie a esigenze specifiche possono usare la funzionalità di base senza incorrere in problemi imprevisti. Ad esempio, molte delle esportazioni Mscoree. dll verrà associato a un oggetto CLR specifico, anche se un metodo potrà non richiederlo. Il [METAHOST_POLICY_FLAGS](../../../../docs/framework/unmanaged-api/hosting/metahost-policy-flags-enumeration.md) enumerazione fornisce i criteri di associazione che sono comuni alla maggior parte degli host.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** Vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** MetaHost.h  
  
 **Libreria:** Inclusa come risorsa in Mscoree. dll  
  
 **Versioni di .NET Framework:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche
- [Interfacce di hosting CLR aggiunte in .NET Framework 4 e 4.5](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [Interfacce di hosting](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [Hosting](../../../../docs/framework/unmanaged-api/hosting/index.md)
