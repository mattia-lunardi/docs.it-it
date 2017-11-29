---
title: Metodo ICorProfilerCallback::RuntimeSuspendAborted
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.RuntimeSuspendAborted
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::RuntimeSuspendAborted
helpviewer_keywords:
- ICorProfilerCallback::RuntimeSuspendAborted method [.NET Framework profiling]
- RuntimeSuspendAborted method [.NET Framework profiling]
ms.assetid: 5a8a4277-345b-448b-a028-fc8cff9998aa
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 2d1c181a471763ea0220c081d64af915ca6be149
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallbackruntimesuspendaborted-method"></a><span data-ttu-id="a51a8-102">Metodo ICorProfilerCallback::RuntimeSuspendAborted</span><span class="sxs-lookup"><span data-stu-id="a51a8-102">ICorProfilerCallback::RuntimeSuspendAborted Method</span></span>
<span data-ttu-id="a51a8-103">Notifica al profiler che il runtime ha interrotto la sospensione di runtime che è stato in corso.</span><span class="sxs-lookup"><span data-stu-id="a51a8-103">Notifies the profiler that the runtime has aborted the runtime suspension that was occurring.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a51a8-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a51a8-104">Syntax</span></span>  
  
```  
HRESULT RuntimeSuspendAborted();  
```  
  
## <a name="remarks"></a><span data-ttu-id="a51a8-105">Note</span><span class="sxs-lookup"><span data-stu-id="a51a8-105">Remarks</span></span>  
 <span data-ttu-id="a51a8-106">La sospensione della fase di esecuzione potrebbe essere interrotto se due thread tentano contemporaneamente di sospendere il runtime.</span><span class="sxs-lookup"><span data-stu-id="a51a8-106">The run-time suspension might be aborted if two threads simultaneously attempt to suspend the runtime.</span></span>  
  
 <span data-ttu-id="a51a8-107">Entrambi i [ICorProfilerCallback:: RuntimeSuspendFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendfinished-method.md) callback o `RuntimeSuspendAborted` richiamata verrà eseguita in un solo thread dopo una [ICorProfilerCallback:: RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) callback.</span><span class="sxs-lookup"><span data-stu-id="a51a8-107">Either the [ICorProfilerCallback::RuntimeSuspendFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendfinished-method.md) callback or the `RuntimeSuspendAborted` callback will occur on a single thread following a [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) callback.</span></span>  
  
 <span data-ttu-id="a51a8-108">Il `RuntimeSuspendAborted` è garantito che si verifichi sullo stesso thread del callback di `RuntimeSuspendStarted` callback.</span><span class="sxs-lookup"><span data-stu-id="a51a8-108">The `RuntimeSuspendAborted` callback is guaranteed to occur on the same thread as the `RuntimeSuspendStarted` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a51a8-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a51a8-109">Requirements</span></span>  
 <span data-ttu-id="a51a8-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a51a8-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a51a8-111">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a51a8-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a51a8-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a51a8-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a51a8-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a51a8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a51a8-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a51a8-114">See Also</span></span>  
 [<span data-ttu-id="a51a8-115">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="a51a8-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)