---
title: Metodo ICorProfilerCallback2::FinalizeableObjectQueued
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback2.FinalizeableObjectQueued
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback2::FinalizeableObjectQueued
helpviewer_keywords:
- FinalizeableObjectQueued method [.NET Framework profiling]
- ICorProfilerCallback2::FinalizeableObjectQueued method [.NET Framework profiling]
ms.assetid: 92d76893-683c-475d-9996-5bff03cdb10f
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 7ff90fd6df337f7b92a73b43b6abc488da7ed6b7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallback2finalizeableobjectqueued-method"></a><span data-ttu-id="2c3fd-102">Metodo ICorProfilerCallback2::FinalizeableObjectQueued</span><span class="sxs-lookup"><span data-stu-id="2c3fd-102">ICorProfilerCallback2::FinalizeableObjectQueued Method</span></span>
<span data-ttu-id="2c3fd-103">Notifica al profiler di codice che un oggetto con un finalizzatore è stato accodato per il thread del finalizzatore per l'esecuzione del relativo `Finalize` metodo.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-103">Notifies the code profiler that an object with a finalizer has been queued to the finalizer thread for execution of its `Finalize` method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c3fd-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c3fd-104">Syntax</span></span>  
  
```  
HRESULT FinalizeableObjectQueued(  
    [in] DWORD finalizerFlags,  
    [in] ObjectID objectID);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2c3fd-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c3fd-105">Parameters</span></span>  
 `finalizerFlags`  
 <span data-ttu-id="2c3fd-106">[in] Il valore di [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) enumerazione che descrive gli aspetti del finalizzatore.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-106">[in] A value of the [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) enumeration that describes aspects of the finalizer.</span></span>  
  
 `objectID`  
 <span data-ttu-id="2c3fd-107">[in] L'ID dell'oggetto che è stata accodata.</span><span class="sxs-lookup"><span data-stu-id="2c3fd-107">[in] The ID of the object that has been queued.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c3fd-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c3fd-108">Requirements</span></span>  
 <span data-ttu-id="2c3fd-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2c3fd-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2c3fd-110">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2c3fd-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2c3fd-111">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2c3fd-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2c3fd-112">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c3fd-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c3fd-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2c3fd-113">See Also</span></span>  
 [<span data-ttu-id="2c3fd-114">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="2c3fd-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="2c3fd-115">ICorProfilerCallback2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="2c3fd-115">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)