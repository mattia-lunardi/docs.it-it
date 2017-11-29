---
title: Metodo IHostAssemblyManager::GetNonHostStoreAssemblies
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostAssemblyManager.GetNonHostStoreAssemblies
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostAssemblyManager::GetNonHostStoreAssemblies
helpviewer_keywords:
- IHostAssemblyManager::GetNonHostStoreAssemblies method [.NET Framework hosting]
- GetNonHostStoreAssemblies method [.NET Framework hosting]
ms.assetid: d2250b38-c76a-40ce-80c8-ba45149886e8
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 35e22e186b290cc4242275976f5109b73e2cf068
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ihostassemblymanagergetnonhoststoreassemblies-method"></a><span data-ttu-id="72b60-102">Metodo IHostAssemblyManager::GetNonHostStoreAssemblies</span><span class="sxs-lookup"><span data-stu-id="72b60-102">IHostAssemblyManager::GetNonHostStoreAssemblies Method</span></span>
<span data-ttu-id="72b60-103">Ottiene un puntatore a interfaccia a un [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) che rappresenta l'elenco di assembly che dovranno essere caricati da common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="72b60-103">Gets an interface pointer to an [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) that represents the list of assemblies that the host expects the common language runtime (CLR) to load.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72b60-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72b60-104">Syntax</span></span>  
  
```  
HRESULT GetNonHostStoreAssemblies (  
    [out] ICLRAssemblyReferenceList **ppReferenceList  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="72b60-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="72b60-105">Parameters</span></span>  
 `ppReferenceList`  
 <span data-ttu-id="72b60-106">[out] Un puntatore all'indirizzo di un `ICLRAssemblyReferenceList` che contiene un elenco di riferimenti agli assembly che dovranno essere caricati da Common Language Runtime da caricare.</span><span class="sxs-lookup"><span data-stu-id="72b60-106">[out] A pointer to the address of an `ICLRAssemblyReferenceList` that contains a list of references to assemblies that the host expects the CLR to load.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="72b60-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72b60-107">Return Value</span></span>  
  
|<span data-ttu-id="72b60-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="72b60-108">HRESULT</span></span>|<span data-ttu-id="72b60-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72b60-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="72b60-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="72b60-110">S_OK</span></span>|<span data-ttu-id="72b60-111">`GetNonHostStoreAssemblies`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="72b60-111">`GetNonHostStoreAssemblies` returned successfully.</span></span>|  
|<span data-ttu-id="72b60-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="72b60-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="72b60-113">CLR non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="72b60-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="72b60-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="72b60-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="72b60-115">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="72b60-115">The call timed out.</span></span>|  
|<span data-ttu-id="72b60-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="72b60-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="72b60-117">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="72b60-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="72b60-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="72b60-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="72b60-119">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="72b60-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="72b60-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="72b60-120">E_FAIL</span></span>|<span data-ttu-id="72b60-121">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="72b60-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="72b60-122">Quando un metodo viene restituito E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="72b60-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="72b60-123">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="72b60-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="72b60-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="72b60-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="72b60-125">Memoria insufficiente è disponibile per creare l'elenco di riferimenti per la richiesta `ICLRAssemblyReferenceList`.</span><span class="sxs-lookup"><span data-stu-id="72b60-125">Not enough memory was available to create the list of references for the requested `ICLRAssemblyReferenceList`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="72b60-126">Note</span><span class="sxs-lookup"><span data-stu-id="72b60-126">Remarks</span></span>  
 <span data-ttu-id="72b60-127">CLR risolve i riferimenti utilizzando le seguenti linee guida:</span><span class="sxs-lookup"><span data-stu-id="72b60-127">The CLR resolves references using the following set of guidelines:</span></span>  
  
-   <span data-ttu-id="72b60-128">Innanzitutto, consulta l'elenco di riferimenti ad assembly restituito da `GetNonHostStoreAssemblies`.</span><span class="sxs-lookup"><span data-stu-id="72b60-128">First, it consults the list of assembly references returned by `GetNonHostStoreAssemblies`.</span></span>  
  
-   <span data-ttu-id="72b60-129">Se l'assembly viene visualizzato nell'elenco, CLR esegue l'associazione normalmente.</span><span class="sxs-lookup"><span data-stu-id="72b60-129">If the assembly appears in the list, the CLR binds to it normally.</span></span>  
  
-   <span data-ttu-id="72b60-130">Se l'assembly non vengono visualizzati nell'elenco e l'host ha fornito un'implementazione di [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md), CLR chiama [IHostAssemblyStore::](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md) per consentire all'host di fornire il assembly da associare.</span><span class="sxs-lookup"><span data-stu-id="72b60-130">If the assembly does not appear in the list and the host has provided an implementation of [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md), the CLR calls [IHostAssemblyStore::ProvideAssembly](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md) to allow the host to supply the assembly to bind to.</span></span>  
  
-   <span data-ttu-id="72b60-131">In caso contrario, CLR non riesce ad associare all'assembly.</span><span class="sxs-lookup"><span data-stu-id="72b60-131">Otherwise, the CLR fails to bind to the assembly.</span></span>  
  
 <span data-ttu-id="72b60-132">Se l'host imposta `ppReferenceList` su null, CLR esamina innanzitutto la global assembly cache, chiama `ProvideAssembly`e quindi analizza la base dell'applicazione per risolvere un riferimento all'assembly.</span><span class="sxs-lookup"><span data-stu-id="72b60-132">If the host sets `ppReferenceList` to null, the CLR first probes the global assembly cache, calls `ProvideAssembly`, and then probes the application base to resolve an assembly reference.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="72b60-133">Al momento dell'inizializzazione, CLR chiama `GetNonHostStoreAssemblies` una sola volta.</span><span class="sxs-lookup"><span data-stu-id="72b60-133">Upon initialization, the CLR calls `GetNonHostStoreAssemblies` only once.</span></span> <span data-ttu-id="72b60-134">Il metodo non viene chiamato nuovamente.</span><span class="sxs-lookup"><span data-stu-id="72b60-134">The method is not called again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72b60-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72b60-135">Requirements</span></span>  
 <span data-ttu-id="72b60-136">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="72b60-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72b60-137">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="72b60-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="72b60-138">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="72b60-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="72b60-139">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72b60-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72b60-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="72b60-140">See Also</span></span>  
 [<span data-ttu-id="72b60-141">ICLRAssemblyReferenceList (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="72b60-141">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)  
 [<span data-ttu-id="72b60-142">IHostAssemblyManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="72b60-142">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
 [<span data-ttu-id="72b60-143">IHostAssemblyStore (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="72b60-143">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)