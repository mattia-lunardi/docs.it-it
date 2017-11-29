---
title: Funzione CorLaunchApplication
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorLaunchApplication
api_location:
- mscoree.dll
- clr.dll
api_type: COM
f1_keywords: CorLaunchApplication
helpviewer_keywords: CorLaunchApplication function [.NET Framework hosting]
ms.assetid: 71f362a9-8fe2-47ce-9302-05a645cf3d7d
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d6246ab600438e2237dcbe531d9d7641c0897d81
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="corlaunchapplication-function"></a><span data-ttu-id="a0587-102">Funzione CorLaunchApplication</span><span class="sxs-lookup"><span data-stu-id="a0587-102">CorLaunchApplication Function</span></span>
<span data-ttu-id="a0587-103">Avvia l'applicazione in corrispondenza del percorso di rete specificato, utilizzando i manifesti specificati e altri dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0587-103">Starts the application at the specified network path, using the specified manifests and other application data.</span></span>  
  
 <span data-ttu-id="a0587-104">Questa funzione è stata deprecata nel [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="a0587-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0587-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0587-105">Syntax</span></span>  
  
```  
HRESULT CorLaunchApplication (  
    [in]  HOST_TYPE                dwClickOnceHost,  
    [in]  LPCWSTR                  pwzAppFullName,  
    [in]  DWORD                    dwManifestPaths,  
    [in]  LPCWSTR                 *ppwzManifestPaths,  
    [in]  DWORD                    dwActivationData,  
    [in]  LPCWSTR                 *ppwzActivationData,  
    [out] LPPROCESS_INFORMATION    lpProcessInformation  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a0587-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0587-106">Parameters</span></span>  
 `dwClickOnceHost`  
 <span data-ttu-id="a0587-107">[in] Il valore di [HOST_TYPE](../../../../docs/framework/unmanaged-api/hosting/host-type-enumeration.md) enumerazione che specifica il tipo di host che sta avviando l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0587-107">[in] A value of the [HOST_TYPE](../../../../docs/framework/unmanaged-api/hosting/host-type-enumeration.md) enumeration that specifies the type of host that is launching the application.</span></span>  
  
 `pwzAppFullName`  
 <span data-ttu-id="a0587-108">[in] Il nome completo dell'applicazione che si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="a0587-108">[in] The full name of the application that is being launched.</span></span>  
  
 `dwManifestPaths`  
 <span data-ttu-id="a0587-109">[in] Il numero di percorsi di manifesto per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0587-109">[in] The number of manifest paths for the application.</span></span>  
  
 `ppwzManifestPaths`  
 <span data-ttu-id="a0587-110">[in] Matrice di stringhe, ognuna delle quali specifica un percorso di un manifesto dell'applicazione che si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="a0587-110">[in] An array of strings, each of which specifies a path to a manifest for the application that is being launched.</span></span>  
  
 `dwActivationData`  
 <span data-ttu-id="a0587-111">[in] Il numero di elementi di dati di attivazione per l'applicazione che si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="a0587-111">[in] The number of activation data items for the application that is being launched.</span></span>  
  
 `ppwzActivationData`  
 <span data-ttu-id="a0587-112">[in] Matrice di stringhe, ognuna delle quali è un elemento di dati di attivazione per l'applicazione che si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="a0587-112">[in] An array of strings, each of which is an activation data item for the application that is being launched.</span></span>  
  
 `lpProcessInformation`  
 <span data-ttu-id="a0587-113">[out] Puntatore alle informazioni sul processo in cui è stata caricata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0587-113">[out] A pointer to information about the process in which the application has been loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0587-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0587-114">Requirements</span></span>  
 <span data-ttu-id="a0587-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a0587-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0587-116">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="a0587-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a0587-117">**Libreria:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a0587-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a0587-118">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0587-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0587-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a0587-119">See Also</span></span>  
 [<span data-ttu-id="a0587-120">Funzioni di Hosting CLR deprecate</span><span class="sxs-lookup"><span data-stu-id="a0587-120">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)