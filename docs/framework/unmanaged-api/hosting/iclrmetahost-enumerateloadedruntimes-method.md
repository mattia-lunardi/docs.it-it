---
title: Metodo ICLRMetaHost::EnumerateLoadedRuntimes
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRMetaHost.EnumerateLoadedRuntimes
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRMetaHost::EnumerateLoadedRuntimes
helpviewer_keywords:
- EnumerateLoadedRuntimes method [.NET Framework hosting]
- ICLRMetaHost::EnumerateLoadedRuntimes method [.NET Framework hosting]
ms.assetid: 22fc0a3f-dce4-4766-9a3c-9fab15f4b4ca
topic_type: apiref
caps.latest.revision: "21"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e0724bf44eaf82b39262876ea4a44509b6c7d576
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="iclrmetahostenumerateloadedruntimes-method"></a><span data-ttu-id="637ae-102">Metodo ICLRMetaHost::EnumerateLoadedRuntimes</span><span class="sxs-lookup"><span data-stu-id="637ae-102">ICLRMetaHost::EnumerateLoadedRuntimes Method</span></span>
<span data-ttu-id="637ae-103">Restituisce un'enumerazione che include un valore valido [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) puntatore a interfaccia per ogni versione di common language runtime (CLR) che viene caricato in un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="637ae-103">Returns an enumeration that includes a valid [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface pointer for each version of the common language runtime (CLR) that is loaded in a given process.</span></span> <span data-ttu-id="637ae-104">Questo metodo sostituisce il [GetVersionFromProcess](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md) (funzione).</span><span class="sxs-lookup"><span data-stu-id="637ae-104">This method supersedes the [GetVersionFromProcess](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="637ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="637ae-105">Syntax</span></span>  
  
```  
HRESULT EnumerateLoadedRuntimes (  
    [in] HANDLE hndProcess,  
    [out, retval] IEnumUnknown **ppEnumerator  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="637ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="637ae-106">Parameters</span></span>  
 `hndProcess`  
 <span data-ttu-id="637ae-107">[in] L'handle del processo per esaminare i runtime caricati.</span><span class="sxs-lookup"><span data-stu-id="637ae-107">[in] The handle of the process to inspect for loaded runtimes.</span></span>  
  
 `ppEnumerator`  
 <span data-ttu-id="637ae-108">[out] Un <!--zz <xref:Microsoft.VisualStudio.OLE.Interop.IEnumUnknown>--> `Microsoft.VisualStudio.OLE.Interop.IEnumUnknown` enumerazione di [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfacce che corrispondono a ogni CLR caricati dal processo.</span><span class="sxs-lookup"><span data-stu-id="637ae-108">[out] An <!--zz <xref:Microsoft.VisualStudio.OLE.Interop.IEnumUnknown>--> `Microsoft.VisualStudio.OLE.Interop.IEnumUnknown` enumeration of [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces corresponding to each CLR that is loaded by the process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="637ae-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="637ae-109">Return Value</span></span>  
 <span data-ttu-id="637ae-110">Questo metodo restituisce gli specifici HRESULT seguenti, nonché gli errori di HRESULT che indicano la mancata riuscita del metodo.</span><span class="sxs-lookup"><span data-stu-id="637ae-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="637ae-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="637ae-111">HRESULT</span></span>|<span data-ttu-id="637ae-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="637ae-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="637ae-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="637ae-113">S_OK</span></span>|<span data-ttu-id="637ae-114">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="637ae-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="637ae-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="637ae-115">E_POINTER</span></span>|<span data-ttu-id="637ae-116">`ppEnumerator` è null.</span><span class="sxs-lookup"><span data-stu-id="637ae-116">`ppEnumerator` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="637ae-117">Note</span><span class="sxs-lookup"><span data-stu-id="637ae-117">Remarks</span></span>  
 <span data-ttu-id="637ae-118">Questo metodo è Elenca tutti i runtime caricati, anche se sono stati caricati con le funzioni deprecate come [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md).</span><span class="sxs-lookup"><span data-stu-id="637ae-118">This method is lists all loaded runtimes, even if they were loaded with deprecated functions such as [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="637ae-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="637ae-119">Requirements</span></span>  
 <span data-ttu-id="637ae-120">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="637ae-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="637ae-121">**Intestazione:** Metahost. H</span><span class="sxs-lookup"><span data-stu-id="637ae-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="637ae-122">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="637ae-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="637ae-123">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="637ae-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="637ae-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="637ae-124">See Also</span></span>  
 [<span data-ttu-id="637ae-125">ICLRMetaHost (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="637ae-125">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)  
 [<span data-ttu-id="637ae-126">Hosting</span><span class="sxs-lookup"><span data-stu-id="637ae-126">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)