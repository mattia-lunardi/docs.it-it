---
title: Metodo ICLRAppDomainResourceMonitor::GetCurrentCpuTime
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor.GetCurrentCpuTime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentCpuTime
helpviewer_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentCpuTime method [.NET Framework hosting]
- GetCurrentCpuTime method [.NET Framework hosting]
ms.assetid: ebc9cc33-fcd6-4cae-9ecb-ea21c51874e6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 63f5687787a9b0cdb30790b7e80e4160cdf413f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737244"
---
# <a name="iclrappdomainresourcemonitorgetcurrentcputime-method"></a>Metodo ICLRAppDomainResourceMonitor::GetCurrentCpuTime
Ottiene il tempo processore totale che è stato usato da tutti i thread durante l'esecuzione nel dominio dell'applicazione corrente, poiché è stato creato il dominio dell'applicazione.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetCurrentCpuTime([in]  DWORD dwAppDomainId,  
                          [out] ULONGLONG* pMilliseconds);  
```  
  
#### <a name="parameters"></a>Parametri  
 `dwAppDomainId`  
 [in] L'ID del dominio dell'applicazione richiesta.  
  
 `pMilliseconds`  
 [out] Un puntatore per il tempo processore totale che è stato usato da tutti i thread durante l'esecuzione nel dominio applicazione corrente poiché è stato creato il dominio dell'applicazione. Questo parametro può essere `null`.  
  
## <a name="return-value"></a>Valore restituito  
  
|HRESULT|Descrizione|  
|-------------|-----------------|  
|S_OK|Metodo completato correttamente.|  
|COR_E_APPDOMAINUNLOADED|Il dominio dell'applicazione è stato scaricato o non esiste.|  
|E_FAIL|Monitoraggio delle risorse del dominio applicazione non è abilitato.<br /><br /> -oppure-<br /><br /> Tutti gli altri errori.|  
  
## <a name="remarks"></a>Note  
 Questo metodo è l'equivalente gestito di gestita <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType> proprietà.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** Vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** MetaHost.h  
  
 **Libreria:** Inclusa come risorsa in Mscoree. dll  
  
 **Versioni di .NET Framework:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia ICLRAppDomainResourceMonitor](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-interface.md)
- [Interfacce di hosting](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [Monitoraggio delle risorse del dominio dell'applicazione](../../../../docs/standard/garbage-collection/app-domain-resource-monitoring.md)
- [Hosting](../../../../docs/framework/unmanaged-api/hosting/index.md)
