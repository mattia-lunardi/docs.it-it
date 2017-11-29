---
title: Metodo ICLRStrongName::StrongNameGetBlob
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- ICLRStrongName.StrongNameGetBlob
- ICLRStrongName.StrongNameGetBlob
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRStrongName::StrongNameGetBlob
helpviewer_keywords:
- ICLRStrongName::StrongNameGetBlob method [.NET Framework hosting]
- StrongNameGetBlob method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: a24218f8-7196-44be-b7a2-ee9cdd7a85c4
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d4ae90367cb84c97d5964ceb815943249af7b240
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="iclrstrongnamestrongnamegetblob-method"></a><span data-ttu-id="3c795-102">Metodo ICLRStrongName::StrongNameGetBlob</span><span class="sxs-lookup"><span data-stu-id="3c795-102">ICLRStrongName::StrongNameGetBlob Method</span></span>
<span data-ttu-id="3c795-103">Riempie il buffer specificato con la rappresentazione binaria del file eseguibile all'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="3c795-103">Fills the specified buffer with the binary representation of the executable file at the specified address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c795-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c795-104">Syntax</span></span>  
  
```  
HRESULT StrongNameGetBlob (  
    [in]  LPCWSTR    wszFilePath,  
    [in]  BYTE       *pbBlob,  
    [in, out] DWORD  *pcbBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3c795-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c795-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="3c795-106">[in] Un percorso valido per il file eseguibile da caricare.</span><span class="sxs-lookup"><span data-stu-id="3c795-106">[in] A valid path to the executable file to be loaded.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="3c795-107">[in] Buffer in cui caricare il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="3c795-107">[in] The buffer into which to load the executable file.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="3c795-108">[in, out] La richiesta di dimensione massima, in byte, di `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="3c795-108">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="3c795-109">Al momento della restituzione, le dimensioni effettive, in byte, di `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="3c795-109">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3c795-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c795-110">Return Value</span></span>  
 <span data-ttu-id="3c795-111">`S_OK`Se il metodo viene completato correttamente. in caso contrario, un valore HRESULT indicante un errore (vedere [valori HRESULT comuni](http://go.microsoft.com/fwlink/?LinkId=213878) per un elenco).</span><span class="sxs-lookup"><span data-stu-id="3c795-111">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c795-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c795-112">Requirements</span></span>  
 <span data-ttu-id="3c795-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3c795-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c795-114">**Intestazione:** Metahost. H</span><span class="sxs-lookup"><span data-stu-id="3c795-114">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="3c795-115">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3c795-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3c795-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c795-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c795-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c795-117">See Also</span></span>  
 [<span data-ttu-id="3c795-118">StrongNameGetBlobFromImage (metodo)</span><span class="sxs-lookup"><span data-stu-id="3c795-118">StrongNameGetBlobFromImage Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md)  
 [<span data-ttu-id="3c795-119">ICLRStrongName (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3c795-119">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)