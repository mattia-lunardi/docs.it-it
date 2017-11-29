---
title: Metodo ICorProfilerInfo2::GetClassLayout
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo2.GetClassLayout
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo2::GetClassLayout
helpviewer_keywords:
- ICorProfilerInfo2::GetClassLayout method [.NET Framework profiling]
- GetClassLayout method, ICorProfilerInfo2 interface [.NET Framework profiling]
ms.assetid: a3a36987-5666-4e2f-95b5-d0cb246502ec
topic_type: apiref
caps.latest.revision: "21"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 988e9daf54d9b4edd623e2488b68dff007e4495b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo2getclasslayout-method"></a><span data-ttu-id="c4a04-102">Metodo ICorProfilerInfo2::GetClassLayout</span><span class="sxs-lookup"><span data-stu-id="c4a04-102">ICorProfilerInfo2::GetClassLayout Method</span></span>
<span data-ttu-id="c4a04-103">Ottiene le informazioni sul layout, in memoria, dei campi definiti dalla classe specificata.</span><span class="sxs-lookup"><span data-stu-id="c4a04-103">Gets information about the layout, in memory, of the fields defined by the specified class.</span></span> <span data-ttu-id="c4a04-104">In altri termini, questo metodo ottiene gli offset dei campi della classe.</span><span class="sxs-lookup"><span data-stu-id="c4a04-104">That is, this method gets the offsets of the class's fields.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4a04-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4a04-105">Syntax</span></span>  
  
```  
HRESULT GetClassLayout(  
    [in]  ClassID classID,  
    [in, out] COR_FIELD_OFFSET rFieldOffset[],  
    [in]  ULONG cFieldOffset,  
    [out] ULONG *pcFieldOffset,  
    [out] ULONG *pulClassSize);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c4a04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4a04-106">Parameters</span></span>  
 `classID`  
 <span data-ttu-id="c4a04-107">[in] ID della classe per la quale verrà recuperato il layout.</span><span class="sxs-lookup"><span data-stu-id="c4a04-107">[in] The ID of the class for which the layout will be retrieved.</span></span>  
  
 `rFieldOffset`  
 <span data-ttu-id="c4a04-108">[in, out] Matrice di [COR_FIELD_OFFSET](../../../../docs/framework/unmanaged-api/metadata/cor-field-offset-structure.md) strutture, ognuno dei quali contiene i token e gli offset dei campi della classe.</span><span class="sxs-lookup"><span data-stu-id="c4a04-108">[in, out] An array of [COR_FIELD_OFFSET](../../../../docs/framework/unmanaged-api/metadata/cor-field-offset-structure.md) structures, each of which contains the tokens and offsets of the class's fields.</span></span>  
  
 `cFieldOffset`  
 <span data-ttu-id="c4a04-109">[in] Dimensione della matrice `rFieldOffset`.</span><span class="sxs-lookup"><span data-stu-id="c4a04-109">[in] The size of the `rFieldOffset` array.</span></span>  
  
 `pcFieldOffset`  
 <span data-ttu-id="c4a04-110">[out] Puntatore al numero complessivo di elementi disponibili.</span><span class="sxs-lookup"><span data-stu-id="c4a04-110">[out] A pointer to the total number of available elements.</span></span> <span data-ttu-id="c4a04-111">Se il parametro `cFieldOffset` è 0, questo valore indica il numero degli elementi necessari.</span><span class="sxs-lookup"><span data-stu-id="c4a04-111">If `cFieldOffset` is 0, this value indicates the number of elements needed.</span></span>  
  
 `pulClassSize`  
 <span data-ttu-id="c4a04-112">[out] Puntatore a una posizione che contiene la dimensione, in byte, della classe.</span><span class="sxs-lookup"><span data-stu-id="c4a04-112">[out] A pointer to a location that contains the size, in bytes, of the class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c4a04-113">Note</span><span class="sxs-lookup"><span data-stu-id="c4a04-113">Remarks</span></span>  
 <span data-ttu-id="c4a04-114">Il metodo `GetClassLayout` restituisce solo i campi definiti dalla classe stessa.</span><span class="sxs-lookup"><span data-stu-id="c4a04-114">The `GetClassLayout` method returns only the fields defined by the class itself.</span></span> <span data-ttu-id="c4a04-115">Se anche la classe padre della classe ha definito alcuni campi, il profiler deve chiamare il metodo `GetClassLayout` sulla classe padre per ottenere quei campi.</span><span class="sxs-lookup"><span data-stu-id="c4a04-115">If the class's parent class has defined fields as well, the profiler must call `GetClassLayout` on the parent class to obtain those fields.</span></span>  
  
 <span data-ttu-id="c4a04-116">Se si usa `GetClassLayout` con le classi di stringa, il metodo non riuscirà e invierà un codice di errore E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="c4a04-116">If you use `GetClassLayout` with string classes, the method will fail with error code E_INVALIDARG.</span></span> <span data-ttu-id="c4a04-117">Utilizzare [ICorProfilerInfo2:: GetStringLayout](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getstringlayout-method.md) per ottenere informazioni sul layout di una stringa.</span><span class="sxs-lookup"><span data-stu-id="c4a04-117">Use [ICorProfilerInfo2::GetStringLayout](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getstringlayout-method.md) to get information about the layout of a string.</span></span> <span data-ttu-id="c4a04-118">`GetClassLayout` non riuscirà, inoltre, quando chiamato con una classe della matrice.</span><span class="sxs-lookup"><span data-stu-id="c4a04-118">`GetClassLayout` will also fail when called with an array class.</span></span>  
  
 <span data-ttu-id="c4a04-119">Dopo il completamento del metodo `GetClassLayout`, è necessario verificare che il buffer `rFieldOffset` sia abbastanza grande per contenere tutte le strutture `COR_FIELD_OFFSET` disponibili.</span><span class="sxs-lookup"><span data-stu-id="c4a04-119">After `GetClassLayout` returns, you must verify that the `rFieldOffset` buffer was large enough to contain all the available `COR_FIELD_OFFSET` structures.</span></span> <span data-ttu-id="c4a04-120">A tale scopo, confrontare il valore a cui punta il parametro `pcFieldOffset` con la dimensione del parametro `rFieldOffset` diviso la dimensione di una struttura `COR_FIELD_OFFSET`.</span><span class="sxs-lookup"><span data-stu-id="c4a04-120">To do this, compare the value that `pcFieldOffset` points to with the size of `rFieldOffset` divided by the size of a `COR_FIELD_OFFSET` structure.</span></span> <span data-ttu-id="c4a04-121">Se il parametro `rFieldOffset` non è abbastanza grande, allocare un buffer `rFieldOffset` più grande, aggiornare `cFieldOffset` con la nuova dimensione e chiamare nuovamente il metodo `GetClassLayout`.</span><span class="sxs-lookup"><span data-stu-id="c4a04-121">If `rFieldOffset` is not large enough, allocate a larger `rFieldOffset` buffer, update `cFieldOffset` with the new, larger size, and call `GetClassLayout` again.</span></span>  
  
 <span data-ttu-id="c4a04-122">In alternativa, è possibile chiamare innanzitutto `GetClassLayout` con un buffer `rFieldOffset` di lunghezza zero per ottenere le dimensioni del buffer corrette.</span><span class="sxs-lookup"><span data-stu-id="c4a04-122">Alternatively, you can first call `GetClassLayout` with a zero-length `rFieldOffset` buffer to obtain the correct buffer size.</span></span> <span data-ttu-id="c4a04-123">È quindi possibile impostare le dimensioni del buffer sul valore restituito nel parametro `pcFieldOffset` e chiamare nuovamente `GetClassLayout`.</span><span class="sxs-lookup"><span data-stu-id="c4a04-123">You can then set the buffer size to the value returned in `pcFieldOffset` and call `GetClassLayout` again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4a04-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4a04-124">Requirements</span></span>  
 <span data-ttu-id="c4a04-125">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c4a04-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4a04-126">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c4a04-126">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c4a04-127">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c4a04-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c4a04-128">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4a04-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4a04-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c4a04-129">See Also</span></span>  
 [<span data-ttu-id="c4a04-130">Interfaccia ICorProfilerInfo</span><span class="sxs-lookup"><span data-stu-id="c4a04-130">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="c4a04-131">Interfaccia ICorProfilerInfo2</span><span class="sxs-lookup"><span data-stu-id="c4a04-131">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)  
 [<span data-ttu-id="c4a04-132">Interfacce di profilatura</span><span class="sxs-lookup"><span data-stu-id="c4a04-132">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="c4a04-133">Profilatura</span><span class="sxs-lookup"><span data-stu-id="c4a04-133">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)