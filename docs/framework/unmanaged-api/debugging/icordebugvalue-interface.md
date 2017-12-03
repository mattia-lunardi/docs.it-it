---
title: ICorDebugValue Interface1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugValue
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugValue
helpviewer_keywords: ICorDebugValue interface [.NET Framework debugging]
ms.assetid: b2f7007f-c446-4b18-aed1-a25cff8aee31
topic_type: apiref
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 01c94df1d8e6ddef0110268461a2b28f594201b6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugvalue-interface1"></a><span data-ttu-id="3519f-102">ICorDebugValue Interface1</span><span class="sxs-lookup"><span data-stu-id="3519f-102">ICorDebugValue Interface1</span></span>
<span data-ttu-id="3519f-103">Rappresenta un valore nel processo sottoposto a debug.</span><span class="sxs-lookup"><span data-stu-id="3519f-103">Represents a value in the process being debugged.</span></span> <span data-ttu-id="3519f-104">Il valore può essere un'operazione di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="3519f-104">The value can be a read or a write value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3519f-105">Metodi</span><span class="sxs-lookup"><span data-stu-id="3519f-105">Methods</span></span>  
  
|<span data-ttu-id="3519f-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="3519f-106">Method</span></span>|<span data-ttu-id="3519f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3519f-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3519f-108">CreateBreakpoint (metodo)</span><span class="sxs-lookup"><span data-stu-id="3519f-108">CreateBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-createbreakpoint-method.md)|<span data-ttu-id="3519f-109">Questo metodo non è attualmente implementato.</span><span class="sxs-lookup"><span data-stu-id="3519f-109">This method is not currently implemented.</span></span>|  
|[<span data-ttu-id="3519f-110">GetAddress (metodo)</span><span class="sxs-lookup"><span data-stu-id="3519f-110">GetAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getaddress-method.md)|<span data-ttu-id="3519f-111">Ottiene l'indirizzo di questo `ICorDebugValue` oggetto, che è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="3519f-111">Gets the address of this `ICorDebugValue` object, which is in the process of being debugged.</span></span>|  
|[<span data-ttu-id="3519f-112">GetSize (metodo)</span><span class="sxs-lookup"><span data-stu-id="3519f-112">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md)|<span data-ttu-id="3519f-113">Ottiene le dimensioni, in byte, di questo `ICorDebugValue` oggetto.</span><span class="sxs-lookup"><span data-stu-id="3519f-113">Gets the size, in bytes, of this `ICorDebugValue` object.</span></span>|  
|[<span data-ttu-id="3519f-114">GetType (metodo)</span><span class="sxs-lookup"><span data-stu-id="3519f-114">GetType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md)|<span data-ttu-id="3519f-115">Ottiene il tipo primitivo di `ICorDebugValue` oggetto.</span><span class="sxs-lookup"><span data-stu-id="3519f-115">Gets the primitive type of this `ICorDebugValue` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3519f-116">Note</span><span class="sxs-lookup"><span data-stu-id="3519f-116">Remarks</span></span>  
 <span data-ttu-id="3519f-117">In generale, la proprietà di un oggetto di valore viene passata quando viene restituita.</span><span class="sxs-lookup"><span data-stu-id="3519f-117">In general, ownership of a value object is passed when it is returned.</span></span> <span data-ttu-id="3519f-118">Il destinatario è responsabile della rimozione di un riferimento dall'oggetto quando viene terminato con l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3519f-118">The recipient is responsible for removing a reference from the object when it is finished with the object.</span></span>  
  
 <span data-ttu-id="3519f-119">A seconda di dove è stato recuperato il valore da, il valore potrebbe non rimanere valido, dopo il processo viene ripreso.</span><span class="sxs-lookup"><span data-stu-id="3519f-119">Depending on where the value was retrieved from, the value may not remain valid after the process is resumed.</span></span> <span data-ttu-id="3519f-120">In tal caso, in generale, il valore non deve essere mantenuto in una chiamata di [ICorDebugController:: Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="3519f-120">So, in general, the value shouldn't be held across a call of the [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3519f-121">Questa interfaccia non supporta la chiamata in modalità remota, tra computer o tra processi.</span><span class="sxs-lookup"><span data-stu-id="3519f-121">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3519f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3519f-122">Requirements</span></span>  
 <span data-ttu-id="3519f-123">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3519f-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3519f-124">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="3519f-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3519f-125">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3519f-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3519f-126">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3519f-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3519f-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3519f-127">See Also</span></span>  
    
    
    
    
 [<span data-ttu-id="3519f-128">ICorDebugValue3 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3519f-128">ICorDebugValue3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)  
 [<span data-ttu-id="3519f-129">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="3519f-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)