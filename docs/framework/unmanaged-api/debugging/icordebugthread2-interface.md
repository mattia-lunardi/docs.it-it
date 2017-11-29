---
title: ICorDebugThread2 Interface1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugThread2
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugThread2
helpviewer_keywords: ICorDebugThread2 interface [.NET Framework debugging]
ms.assetid: 678f89f9-cce7-46d1-af87-5e989abaa93c
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5d3a554d075adb56294e4693b234ce22735fb982
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugthread2-interface1"></a><span data-ttu-id="e8eb3-102">ICorDebugThread2 Interface1</span><span class="sxs-lookup"><span data-stu-id="e8eb3-102">ICorDebugThread2 Interface1</span></span>
<span data-ttu-id="e8eb3-103">Opera come estensione logica dell'interfaccia ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="e8eb3-103">Serves as a logical extension to the ICorDebugThread interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e8eb3-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="e8eb3-104">Methods</span></span>  
  
|<span data-ttu-id="e8eb3-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="e8eb3-105">Method</span></span>|<span data-ttu-id="e8eb3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8eb3-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e8eb3-107">GetActiveFunctions (metodo)</span><span class="sxs-lookup"><span data-stu-id="e8eb3-107">GetActiveFunctions Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getactivefunctions-method.md)|<span data-ttu-id="e8eb3-108">Ottiene una matrice di istanze COR_ACTIVE_FUNCTION contenenti dati relativi a funzioni attive nei frame di un thread.</span><span class="sxs-lookup"><span data-stu-id="e8eb3-108">Gets an array of COR_ACTIVE_FUNCTION instances that contain data about the active functions in a thread's frames.</span></span>|  
|[<span data-ttu-id="e8eb3-109">GetConnectionID (metodo)</span><span class="sxs-lookup"><span data-stu-id="e8eb3-109">GetConnectionID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getconnectionid-method.md)|<span data-ttu-id="e8eb3-110">Ottiene un identificatore di connessione per `ICorDebugThread2`.</span><span class="sxs-lookup"><span data-stu-id="e8eb3-110">Gets a connection identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="e8eb3-111">GetTaskID (metodo)</span><span class="sxs-lookup"><span data-stu-id="e8eb3-111">GetTaskID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-gettaskid-method.md)|<span data-ttu-id="e8eb3-112">Ottiene un identificatore di attività per `ICorDebugThread2`.</span><span class="sxs-lookup"><span data-stu-id="e8eb3-112">Gets a task identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="e8eb3-113">GetVolatileOSThreadID (metodo)</span><span class="sxs-lookup"><span data-stu-id="e8eb3-113">GetVolatileOSThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getvolatileosthreadid-method.md)|<span data-ttu-id="e8eb3-114">Ottiene l'identificatore del thread del sistema operativo per `ICorDebugThread2`.</span><span class="sxs-lookup"><span data-stu-id="e8eb3-114">Gets the operating system thread identifier for this `ICorDebugThread2`.</span></span>|  
|[<span data-ttu-id="e8eb3-115">InterceptCurrentException (metodo)</span><span class="sxs-lookup"><span data-stu-id="e8eb3-115">InterceptCurrentException Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-interceptcurrentexception-method.md)|<span data-ttu-id="e8eb3-116">Consente a un debugger intercettare l'eccezione corrente in un thread.</span><span class="sxs-lookup"><span data-stu-id="e8eb3-116">Allows a debugger to intercept the current exception on a thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e8eb3-117">Note</span><span class="sxs-lookup"><span data-stu-id="e8eb3-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e8eb3-118">Questa interfaccia non supporta la chiamata in modalità remota, tra computer o tra processi.</span><span class="sxs-lookup"><span data-stu-id="e8eb3-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8eb3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8eb3-119">Requirements</span></span>  
 <span data-ttu-id="e8eb3-120">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8eb3-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8eb3-121">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="e8eb3-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e8eb3-122">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8eb3-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8eb3-123">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8eb3-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8eb3-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e8eb3-124">See Also</span></span>  
 [<span data-ttu-id="e8eb3-125">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="e8eb3-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)