---
title: Metodo ICorProfilerInfo4::GetCodeInfo3
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo4.GetCodeInfo3
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo4::GetCodeInfo3
helpviewer_keywords:
- GetCodeInfo3 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetCodeInfo3 method [.NET Framework profiling]
ms.assetid: bb8c105e-4d9a-4684-8c05-ed6909cc1b8c
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 87a93220bbaf3930f8ac2671efc0f19b2df8aee5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo4getcodeinfo3-method"></a><span data-ttu-id="76b8b-102">Metodo ICorProfilerInfo4::GetCodeInfo3</span><span class="sxs-lookup"><span data-stu-id="76b8b-102">ICorProfilerInfo4::GetCodeInfo3 Method</span></span>
<span data-ttu-id="76b8b-103">Ottiene gli ambiti di codice nativo associati alla versione ricompilata in JIT della funzione specificata.</span><span class="sxs-lookup"><span data-stu-id="76b8b-103">Gets the extents of native code associated with the JIT-recompiled version of the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76b8b-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76b8b-104">Syntax</span></span>  
  
```  
HRESULT GetCodeInfo3(  
    [in]  FunctionID functionID,  
    [in]  ReJITID reJitId,  
    [in]  ULONG32 cCodeInfos,  
    [out] ULONG32 *pcCodeInfos,  
    [out, size_is(cCodeInfos), length_is(*pcCodeInfos)]  
    COR_PRF_CODE_INFO codeInfos[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="76b8b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="76b8b-105">Parameters</span></span>  
 `functionID`  
 <span data-ttu-id="76b8b-106">[in] ID della funzione alla quale è associato il codice nativo.</span><span class="sxs-lookup"><span data-stu-id="76b8b-106">[in] The ID of the function with which the native code is associated.</span></span>  
  
 `reJitId`  
 <span data-ttu-id="76b8b-107">[in] Identità della funzione ricompilata in JIT.</span><span class="sxs-lookup"><span data-stu-id="76b8b-107">[in] The identity of the JIT-recompiled function.</span></span>  
  
 `cCodeInfos`  
 <span data-ttu-id="76b8b-108">[in] Dimensione della matrice `codeInfos`.</span><span class="sxs-lookup"><span data-stu-id="76b8b-108">[in] The size of the `codeInfos` array.</span></span>  
  
 `pcCodeInfos`  
 <span data-ttu-id="76b8b-109">[out] Un puntatore al numero totale di [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) strutture disponibili.</span><span class="sxs-lookup"><span data-stu-id="76b8b-109">[out] A pointer to the total number of [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) structures available.</span></span>  
  
 `codeInfos`  
 <span data-ttu-id="76b8b-110">[out] Buffer fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="76b8b-110">[out] A caller-provided buffer.</span></span> <span data-ttu-id="76b8b-111">Una volta completato, il metodo contiene una matrice di strutture `COR_PRF_CODE_INFO`, ognuna delle quali descrive un blocco di codice nativo.</span><span class="sxs-lookup"><span data-stu-id="76b8b-111">After the method returns, it contains an array of `COR_PRF_CODE_INFO` structures, each of which describes a block of native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="76b8b-112">Note</span><span class="sxs-lookup"><span data-stu-id="76b8b-112">Remarks</span></span>  
 <span data-ttu-id="76b8b-113">Il `GetCodeInfo3` è simile al metodo [GetCodeInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md), ad eccezione del fatto che ottiene l'ID ricompilata in JIT della funzione che contiene l'indirizzo IP specificato.</span><span class="sxs-lookup"><span data-stu-id="76b8b-113">The `GetCodeInfo3` method is similar to [GetCodeInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md), except that it will get the JIT-recompiled ID of the function that contains the specified IP address.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="76b8b-114">`GetCodeInfo3`può attivare una garbage collection, mentre [GetCodeInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md) No.</span><span class="sxs-lookup"><span data-stu-id="76b8b-114">`GetCodeInfo3` can trigger a garbage collection, whereas [GetCodeInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md) will not.</span></span> <span data-ttu-id="76b8b-115">Per ulteriori informazioni, vedere il [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE](../../../../docs/framework/unmanaged-api/profiling/corprof-e-unsupported-call-sequence-hresult.md) HRESULT.</span><span class="sxs-lookup"><span data-stu-id="76b8b-115">For more information, see the [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE](../../../../docs/framework/unmanaged-api/profiling/corprof-e-unsupported-call-sequence-hresult.md) HRESULT.</span></span>  
  
 <span data-ttu-id="76b8b-116">Gli ambiti vengono ordinati in sequenza crescente in base all'offset CIL (Common Intermediate Language).</span><span class="sxs-lookup"><span data-stu-id="76b8b-116">The extents are sorted in order of increasing Common Intermediate Language (CIL) offset.</span></span>  
  
 <span data-ttu-id="76b8b-117">Dopo `GetCodeInfo3` viene restituito, è necessario verificare che il `codeInfos` buffer sia abbastanza grande per contenere tutti i [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) strutture.</span><span class="sxs-lookup"><span data-stu-id="76b8b-117">After `GetCodeInfo3` returns, you must verify that the `codeInfos` buffer was large enough to contain all the [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) structures.</span></span> <span data-ttu-id="76b8b-118">A tale scopo, confrontare il valore di `cCodeInfos` con il valore del parametro `cchName`.</span><span class="sxs-lookup"><span data-stu-id="76b8b-118">To do this, compare the value of `cCodeInfos` with the value of the `cchName` parameter.</span></span> <span data-ttu-id="76b8b-119">Se `cCodeInfos` diviso la dimensione di un [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) struttura è inferiore a `pcCodeInfos`, allocare una maggiore `codeInfos` memorizzare nel buffer, aggiornare `cCodeInfos` con la nuova dimensione e chiamare `GetCodeInfo3` nuovo.</span><span class="sxs-lookup"><span data-stu-id="76b8b-119">If `cCodeInfos` divided by the size of a [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) structure is smaller than `pcCodeInfos`, allocate a larger `codeInfos` buffer, update `cCodeInfos` with the new, larger size, and call `GetCodeInfo3` again.</span></span>  
  
 <span data-ttu-id="76b8b-120">In alternativa, è possibile chiamare innanzitutto `GetCodeInfo3` con un buffer `codeInfos` di lunghezza zero per ottenere le dimensioni del buffer corrette.</span><span class="sxs-lookup"><span data-stu-id="76b8b-120">Alternatively, you can first call `GetCodeInfo3` with a zero-length `codeInfos` buffer to obtain the correct buffer size.</span></span> <span data-ttu-id="76b8b-121">È quindi possibile impostare il `codeInfos` il valore restituito in dimensioni del buffer `pcCodeInfos`, moltiplicato per la dimensione di un [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) struttura e chiamare `GetCodeInfo3` nuovamente.</span><span class="sxs-lookup"><span data-stu-id="76b8b-121">You can then set the `codeInfos` buffer size to the value returned in `pcCodeInfos`, multiplied by the size of a [COR_PRF_CODE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-code-info-structure.md) structure, and call `GetCodeInfo3` again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76b8b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76b8b-122">Requirements</span></span>  
 <span data-ttu-id="76b8b-123">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="76b8b-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76b8b-124">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="76b8b-124">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="76b8b-125">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="76b8b-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="76b8b-126">**Versioni di .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76b8b-126">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76b8b-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="76b8b-127">See Also</span></span>  
 [<span data-ttu-id="76b8b-128">GetCodeInfo2 (metodo)</span><span class="sxs-lookup"><span data-stu-id="76b8b-128">GetCodeInfo2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md)  
 [<span data-ttu-id="76b8b-129">ICorProfilerInfo4 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="76b8b-129">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)  
 [<span data-ttu-id="76b8b-130">Interfacce di profilatura</span><span class="sxs-lookup"><span data-stu-id="76b8b-130">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="76b8b-131">Profilatura</span><span class="sxs-lookup"><span data-stu-id="76b8b-131">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)