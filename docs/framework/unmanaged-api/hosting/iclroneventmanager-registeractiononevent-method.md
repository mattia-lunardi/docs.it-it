---
title: Metodo ICLROnEventManager::RegisterActionOnEvent
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLROnEventManager.RegisterActionOnEvent
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLROnEventManager::RegisterActionOnEvent
helpviewer_keywords:
- ICLROnEventManager::RegisterActionOnEvent method [.NET Framework hosting]
- RegisterActionOnEvent method [.NET Framework hosting]
ms.assetid: b944cf49-918d-4c4e-993b-77d097a52550
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0ef99527abc7ca33e1176958a590483f34556a1b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="iclroneventmanagerregisteractiononevent-method"></a><span data-ttu-id="3650a-102">Metodo ICLROnEventManager::RegisterActionOnEvent</span><span class="sxs-lookup"><span data-stu-id="3650a-102">ICLROnEventManager::RegisterActionOnEvent Method</span></span>
<span data-ttu-id="3650a-103">Registra un puntatore di callback per l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="3650a-103">Registers a callback pointer for the specified event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3650a-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3650a-104">Syntax</span></span>  
  
```  
HRESULT RegisterActionOnEvent (  
    [in] EClrEvent event,  
    [in] IActionOnCLREvent *pAction  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3650a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3650a-105">Parameters</span></span>  
 `event`  
 <span data-ttu-id="3650a-106">[in] Uno del [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) valori, che indica l'evento per il quale registrare il puntatore di callback descritto da `pAction`.</span><span class="sxs-lookup"><span data-stu-id="3650a-106">[in] One of the [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) values, indicating the event for which to register the callback pointer described by `pAction`.</span></span>  
  
 `pAction`  
 <span data-ttu-id="3650a-107">[in] Un puntatore a un [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) oggetto che viene chiamato quando viene generato l'evento registrato.</span><span class="sxs-lookup"><span data-stu-id="3650a-107">[in] A pointer to an [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) object that is called when the registered event fires.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3650a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3650a-108">Return Value</span></span>  
  
|<span data-ttu-id="3650a-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3650a-109">HRESULT</span></span>|<span data-ttu-id="3650a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3650a-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3650a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3650a-111">S_OK</span></span>|<span data-ttu-id="3650a-112">`RegisterActionOnEvent`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3650a-112">`RegisterActionOnEvent` returned successfully.</span></span>|  
|<span data-ttu-id="3650a-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3650a-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3650a-114">Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="3650a-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3650a-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3650a-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3650a-116">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="3650a-116">The call timed out.</span></span>|  
|<span data-ttu-id="3650a-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3650a-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3650a-118">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="3650a-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3650a-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3650a-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3650a-120">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="3650a-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3650a-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3650a-121">E_FAIL</span></span>|<span data-ttu-id="3650a-122">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3650a-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3650a-123">Se un metodo restituisce E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="3650a-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3650a-124">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="3650a-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3650a-125">Note</span><span class="sxs-lookup"><span data-stu-id="3650a-125">Remarks</span></span>  
 <span data-ttu-id="3650a-126">L'host può registrare callback per uno o entrambi i tipi di due eventi descritti dal `EClrEvent`.</span><span class="sxs-lookup"><span data-stu-id="3650a-126">The host can register callbacks for either or both of the two event types described by `EClrEvent`.</span></span> <span data-ttu-id="3650a-127">L'host ottiene il `ICLROnEventManager` interfaccia chiamando il [ICLRControl::](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="3650a-127">The host gets the `ICLROnEventManager` interface by calling the [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3650a-128">Gli eventi che `RegisterActionOnEvent` registri possono essere generati più volte da thread diversi per segnalare uno scaricamento o la disattivazione di CLR.</span><span class="sxs-lookup"><span data-stu-id="3650a-128">The events that `RegisterActionOnEvent` registers can be fired more than once and from different threads to signal an unload or the disabling of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3650a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3650a-129">Requirements</span></span>  
 <span data-ttu-id="3650a-130">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3650a-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3650a-131">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="3650a-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3650a-132">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3650a-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3650a-133">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3650a-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3650a-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3650a-134">See Also</span></span>  
 [<span data-ttu-id="3650a-135">Enumerazione EClrEvent</span><span class="sxs-lookup"><span data-stu-id="3650a-135">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)  
 [<span data-ttu-id="3650a-136">IActionOnCLREvent (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3650a-136">IActionOnCLREvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md)  
 [<span data-ttu-id="3650a-137">ICLRControl (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3650a-137">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="3650a-138">ICLROnEventManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3650a-138">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)