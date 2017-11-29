---
title: Interfaccia ICorDebugManagedCallback2
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback2
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback2
helpviewer_keywords: ICorDebugManagedCallback2 interface [.NET Framework debugging]
ms.assetid: cf7b7cfa-1c4b-4d8c-be70-4f9ed15a788b
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0d5b8ac63d200e54d25b58870089f6c062397186
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmanagedcallback2-interface"></a><span data-ttu-id="4fd49-102">Interfaccia ICorDebugManagedCallback2</span><span class="sxs-lookup"><span data-stu-id="4fd49-102">ICorDebugManagedCallback2 Interface</span></span>
<span data-ttu-id="4fd49-103">Fornisce metodi che supportano la gestione delle eccezioni del debugger e assistenti al debug gestito.</span><span class="sxs-lookup"><span data-stu-id="4fd49-103">Provides methods to support debugger exception handling and managed debugging assistants (MDAs).</span></span> <span data-ttu-id="4fd49-104">`ICorDebugManagedCallback2`è un'estensione logica del [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4fd49-104">`ICorDebugManagedCallback2` is a logical extension of the [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4fd49-105">Metodi</span><span class="sxs-lookup"><span data-stu-id="4fd49-105">Methods</span></span>  
  
|<span data-ttu-id="4fd49-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="4fd49-106">Method</span></span>|<span data-ttu-id="4fd49-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd49-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4fd49-108">ChangeConnection (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fd49-108">ChangeConnection Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-changeconnection-method.md)|<span data-ttu-id="4fd49-109">Notifica al debugger che il set di attività associata alla connessione specificata è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="4fd49-109">Notifies the debugger that the set of tasks associated with the specified connection has changed.</span></span>|  
|[<span data-ttu-id="4fd49-110">Metodo CreateConnection</span><span class="sxs-lookup"><span data-stu-id="4fd49-110">CreateConnection Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-createconnection-method.md)|<span data-ttu-id="4fd49-111">Notifica al debugger che è stata creata una nuova connessione.</span><span class="sxs-lookup"><span data-stu-id="4fd49-111">Notifies the debugger that a new connection has been created.</span></span>|  
|[<span data-ttu-id="4fd49-112">DestroyConnection (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fd49-112">DestroyConnection Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-destroyconnection-method.md)|<span data-ttu-id="4fd49-113">Notifica al debugger che la connessione specificata è stata terminata.</span><span class="sxs-lookup"><span data-stu-id="4fd49-113">Notifies the debugger that the specified connection has been terminated.</span></span>|  
|[<span data-ttu-id="4fd49-114">Exception (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fd49-114">Exception Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exception-method.md)|<span data-ttu-id="4fd49-115">Notifica al debugger che si è iniziata una ricerca di un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="4fd49-115">Notifies the debugger that a search for an exception handler has started.</span></span>|  
|[<span data-ttu-id="4fd49-116">ExceptionUnwind (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fd49-116">ExceptionUnwind Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exceptionunwind-method.md)|<span data-ttu-id="4fd49-117">Fornisce una notifica sullo stato durante il processo di rimozione di eccezione.</span><span class="sxs-lookup"><span data-stu-id="4fd49-117">Provides a status notification during the exception unwinding process.</span></span>|  
|[<span data-ttu-id="4fd49-118">FunctionRemapComplete (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fd49-118">FunctionRemapComplete Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapcomplete-method.md)|<span data-ttu-id="4fd49-119">Notifica al debugger che l'esecuzione di codice è passata a una nuova versione di una funzione modificata.</span><span class="sxs-lookup"><span data-stu-id="4fd49-119">Notifies the debugger that code execution has switched to a new version of an edited function.</span></span>|  
|[<span data-ttu-id="4fd49-120">FunctionRemapOpportunity (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fd49-120">FunctionRemapOpportunity Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapopportunity-method.md)|<span data-ttu-id="4fd49-121">Notifica al debugger che l'esecuzione del codice ha raggiunto un punto di sequenza in una versione precedente di una funzione modificata.</span><span class="sxs-lookup"><span data-stu-id="4fd49-121">Notifies the debugger that code execution has reached a sequence point in an older version of an edited function.</span></span>|  
|[<span data-ttu-id="4fd49-122">MDANotification (metodo)</span><span class="sxs-lookup"><span data-stu-id="4fd49-122">MDANotification Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-mdanotification-method.md)|<span data-ttu-id="4fd49-123">Fornisce una notifica che l'esecuzione del codice ha rilevato un messaggio di assistente al debug gestito.</span><span class="sxs-lookup"><span data-stu-id="4fd49-123">Provides notification that code execution has encountered a managed debugging assistant (MDA) message.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4fd49-124">Note</span><span class="sxs-lookup"><span data-stu-id="4fd49-124">Remarks</span></span>  
 <span data-ttu-id="4fd49-125">Il `ICorDebugManagedCallback2` interfaccia estende il `ICorDebugManagedCallback` interfaccia per gestire i nuovi eventi di debug introdotti in .NET Framework versione 2.0.</span><span class="sxs-lookup"><span data-stu-id="4fd49-125">The `ICorDebugManagedCallback2` interface extends the `ICorDebugManagedCallback` interface to handle new debug events introduced in the .NET Framework version 2.0.</span></span>  
  
 <span data-ttu-id="4fd49-126">Un debugger deve implementare `ICorDebugManagedCallback2` se sta eseguendo il debug di applicazioni .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="4fd49-126">A debugger must implement `ICorDebugManagedCallback2` if it is debugging .NET Framework 2.0 applications.</span></span> <span data-ttu-id="4fd49-127">Un'istanza di `ICorDebugManagedCallback` o `ICorDebugManagedCallback2` viene passato come oggetto di callback da [ICorDebug:: SetManagedHandler](../../../../docs/framework/unmanaged-api/debugging/icordebug-setmanagedhandler-method.md).</span><span class="sxs-lookup"><span data-stu-id="4fd49-127">An instance of `ICorDebugManagedCallback` or `ICorDebugManagedCallback2` is passed as the callback object to [ICorDebug::SetManagedHandler](../../../../docs/framework/unmanaged-api/debugging/icordebug-setmanagedhandler-method.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4fd49-128">Questa interfaccia non supporta la chiamata in modalità remota, tra computer o tra processi.</span><span class="sxs-lookup"><span data-stu-id="4fd49-128">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4fd49-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fd49-129">Requirements</span></span>  
 <span data-ttu-id="4fd49-130">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4fd49-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4fd49-131">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="4fd49-131">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4fd49-132">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4fd49-132">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4fd49-133">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4fd49-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fd49-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4fd49-134">See Also</span></span>  
 [<span data-ttu-id="4fd49-135">Diagnostica degli errori tramite gli assistenti al debug gestito</span><span class="sxs-lookup"><span data-stu-id="4fd49-135">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [<span data-ttu-id="4fd49-136">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="4fd49-136">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="4fd49-137">ICorDebugManagedCallback (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="4fd49-137">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)