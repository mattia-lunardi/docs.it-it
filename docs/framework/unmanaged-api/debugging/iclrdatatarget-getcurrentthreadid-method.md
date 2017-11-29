---
title: Metodo ICLRDataTarget::GetCurrentThreadID
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDataTarget.GetCurrentThreadID
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICLRDataTarget::GetCurrentThreadID
helpviewer_keywords:
- GetCurrentThreadID method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::GetCurrentThreadID method [.NET Framework debugging]
ms.assetid: dc9a0a6c-d592-4fb7-86ed-62684da3b0e1
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 3820a3f32834f02b60fb33448bcaf8febdc15ce6
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="iclrdatatargetgetcurrentthreadid-method"></a><span data-ttu-id="8ec0c-102">Metodo ICLRDataTarget::GetCurrentThreadID</span><span class="sxs-lookup"><span data-stu-id="8ec0c-102">ICLRDataTarget::GetCurrentThreadID Method</span></span>
<span data-ttu-id="8ec0c-103">Ottiene l'identificatore del sistema operativo per il thread corrente.</span><span class="sxs-lookup"><span data-stu-id="8ec0c-103">Gets the operating system identifier for the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ec0c-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ec0c-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentThreadID (  
    [out] ULONG32    *threadID  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8ec0c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ec0c-105">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="8ec0c-106">[out] Un puntatore all'identificatore del sistema operativo del thread corrente per il processo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ec0c-106">[out] A pointer to the operating system identifier of the current thread for the target process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8ec0c-107">Note</span><span class="sxs-lookup"><span data-stu-id="8ec0c-107">Remarks</span></span>  
 <span data-ttu-id="8ec0c-108">Se è presente alcun thread corrente per il processo di destinazione, il `GetCurrentThreadID` metodo potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="8ec0c-108">If there is no current thread for the target process, the `GetCurrentThreadID` method may fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ec0c-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ec0c-109">Requirements</span></span>  
 <span data-ttu-id="8ec0c-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ec0c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ec0c-111">**Intestazione:** ClrData.idl, Clrdata. H</span><span class="sxs-lookup"><span data-stu-id="8ec0c-111">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="8ec0c-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ec0c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ec0c-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ec0c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ec0c-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8ec0c-114">See Also</span></span>  
 [<span data-ttu-id="8ec0c-115">ICLRDataTarget (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="8ec0c-115">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)