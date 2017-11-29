---
title: Metodo ICorProfilerCallback::ObjectReferences
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ObjectReferences
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ObjectReferences
helpviewer_keywords:
- ObjectReferences method [.NET Framework profiling]
- ICorProfilerCallback::ObjectReferences method [.NET Framework profiling]
ms.assetid: dd5e9b64-b4a3-4ba6-9be6-ddb540f4ffcf
topic_type: apiref
caps.latest.revision: "18"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5cdebc1984f86d3801759f8f987df8fb89d82e3a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallbackobjectreferences-method"></a><span data-ttu-id="7c31f-102">Metodo ICorProfilerCallback::ObjectReferences</span><span class="sxs-lookup"><span data-stu-id="7c31f-102">ICorProfilerCallback::ObjectReferences Method</span></span>
<span data-ttu-id="7c31f-103">Notifica al profiler gli oggetti in memoria a cui fa riferimento l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="7c31f-103">Notifies the profiler about objects in memory that are being referenced by the specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c31f-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c31f-104">Syntax</span></span>  
  
```  
HRESULT ObjectReferences(  
    [in]  ObjectID objectId,  
    [in]  ClassID  classId,  
    [in]  ULONG    cObjectRefs,  
    [in, size_is(cObjectRefs)] ObjectID objectRefIds[] );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7c31f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c31f-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="7c31f-106">[in] L'ID dell'oggetto cui fa riferimento a oggetti.</span><span class="sxs-lookup"><span data-stu-id="7c31f-106">[in] The ID of the object that is referencing objects.</span></span>  
  
 `classId`  
 <span data-ttu-id="7c31f-107">[in] L'ID della classe che l'oggetto specificato è un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="7c31f-107">[in] The ID of the class that the specified object is an instance of.</span></span>  
  
 `cObjectRefs`  
 <span data-ttu-id="7c31f-108">[in] Il numero di oggetti a cui fa riferimento l'oggetto specificato (ovvero, il numero di elementi nel `objectRefIds` matrice).</span><span class="sxs-lookup"><span data-stu-id="7c31f-108">[in] The number of objects referenced by the specified object (that is, the number of elements in the `objectRefIds` array).</span></span>  
  
 `objectRefIds`  
 <span data-ttu-id="7c31f-109">[in] Matrice di ID di oggetti a cui fa riferimento `objectId`.</span><span class="sxs-lookup"><span data-stu-id="7c31f-109">[in] An array of IDs of objects that are being referenced by `objectId`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7c31f-110">Note</span><span class="sxs-lookup"><span data-stu-id="7c31f-110">Remarks</span></span>  
 <span data-ttu-id="7c31f-111">Il `ObjectReferences` metodo viene chiamato per ogni oggetto rimane nell'heap dopo un'operazione di garbage collection è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7c31f-111">The `ObjectReferences` method is called for each object remaining in the heap after a garbage collection has completed.</span></span> <span data-ttu-id="7c31f-112">Se il profiler restituisce un errore da questo callback, i servizi di profilatura non richiameranno questo callback fino a quando la successiva operazione di garbage collection.</span><span class="sxs-lookup"><span data-stu-id="7c31f-112">If the profiler returns an error from this callback, the profiling services will discontinue invoking this callback until the next garbage collection.</span></span>  
  
 <span data-ttu-id="7c31f-113">Il `ObjectReferences` callback può essere usato in combinazione con il [ICorProfilerCallback:: RootReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md) callback per creare un grafico di riferimento di oggetto completo per il runtime.</span><span class="sxs-lookup"><span data-stu-id="7c31f-113">The `ObjectReferences` callback can be used in conjunction with the [ICorProfilerCallback::RootReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md) callback to create a complete object reference graph for the runtime.</span></span> <span data-ttu-id="7c31f-114">Common language runtime (CLR) garantisce che ogni riferimento all'oggetto venga segnalato solo una volta per il `ObjectReferences` metodo.</span><span class="sxs-lookup"><span data-stu-id="7c31f-114">The common language runtime (CLR) ensures that each object reference is reported only once by the `ObjectReferences` method.</span></span>  
  
 <span data-ttu-id="7c31f-115">L'ID di oggetto restituito da `ObjectReferences` non validi durante il callback vero e proprio, perché l'operazione di garbage collection potrebbe essere ancora spostando gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7c31f-115">The object IDs returned by `ObjectReferences` are not valid during the callback itself, because the garbage collection might be in the middle of moving objects.</span></span> <span data-ttu-id="7c31f-116">Di conseguenza, i profiler non devono tentare di controllare gli oggetti durante una `ObjectReferences` chiamare.</span><span class="sxs-lookup"><span data-stu-id="7c31f-116">Therefore, profilers must not attempt to inspect objects during an `ObjectReferences` call.</span></span> <span data-ttu-id="7c31f-117">Quando [ICorProfilerCallback2::](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md) viene chiamato, l'operazione di garbage collection è stata completata e l'ispezione può essere eseguita in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="7c31f-117">When [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md) is called, the garbage collection is complete and inspection can be safely done.</span></span>  
  
 <span data-ttu-id="7c31f-118">Un valore null `ClassId` indica che `objectId` dispone di un tipo che lo scaricamento.</span><span class="sxs-lookup"><span data-stu-id="7c31f-118">A null `ClassId` indicates that `objectId` has a type that is unloading.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7c31f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c31f-119">Requirements</span></span>  
 <span data-ttu-id="7c31f-120">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7c31f-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7c31f-121">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7c31f-121">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7c31f-122">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7c31f-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7c31f-123">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c31f-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c31f-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7c31f-124">See Also</span></span>  
 [<span data-ttu-id="7c31f-125">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="7c31f-125">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)