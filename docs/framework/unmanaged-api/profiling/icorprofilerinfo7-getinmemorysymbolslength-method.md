---
title: 'Metodo icorprofilerinfo7:: Getinmemorysymbolslength'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
api_name: ICorProfilerInfo7.GetInMemorySymbolsLength
api_location:
- mscorwks.dll
- icorprof.idl
api_type: COM
ms.assetid: d62c4a4c-8a62-45aa-8f01-a8387cf36159
caps.latest.revision: "3"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 34da00bdc33a836e5f459e6e4314f252e1e39e9b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerinfo7getinmemorysymbolslength-method"></a><span data-ttu-id="99fd1-102">Metodo icorprofilerinfo7:: Getinmemorysymbolslength</span><span class="sxs-lookup"><span data-stu-id="99fd1-102">ICorProfilerInfo7::GetInMemorySymbolsLength Method</span></span>
<span data-ttu-id="99fd1-103">[Supportata in .NET Framework 4.6.1 e versioni successive]</span><span class="sxs-lookup"><span data-stu-id="99fd1-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="99fd1-104">Restituisce la lunghezza di un flusso di simboli in memoria.</span><span class="sxs-lookup"><span data-stu-id="99fd1-104">Returns the length of an in-memory symbol stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99fd1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99fd1-105">Syntax</span></span>  
  
```  
HRESULT GetInMemorySymbolsLength(  
        [in] ModuleID moduleId,  
        [out] DWORD* pCountSymbolBytes  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="99fd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99fd1-106">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="99fd1-107">[in] L'identificatore del modulo contenente il flusso in memoria.</span><span class="sxs-lookup"><span data-stu-id="99fd1-107">[in] The identifier of the module containing the in-memory stream.</span></span>  
  
 <span data-ttu-id="99fd1-108">pCountSymbolBytes</span><span class="sxs-lookup"><span data-stu-id="99fd1-108">pCountSymbolBytes</span></span>  
 <span data-ttu-id="99fd1-109">[out] Un puntatore a un `DWORD` valore che, quando il metodo viene restituito, contiene la lunghezza del flusso in byte.</span><span class="sxs-lookup"><span data-stu-id="99fd1-109">[out] A pointer to a `DWORD` value that, when the method returns, contains the length of the stream in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="99fd1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99fd1-110">Return Value</span></span>  
 <span data-ttu-id="99fd1-111">Il metodo restituisce `S_OK` se la lunghezza del flusso di memoria può essere determinata, anche se è zero (0).</span><span class="sxs-lookup"><span data-stu-id="99fd1-111">The method returns `S_OK` if the length of the memory stream can be determined, even if it is zero (0).</span></span>  
  
 <span data-ttu-id="99fd1-112">Il metodo restituisce `CORPROF_E_MODULE_IS_DYNAMIC` se il metodo è stato creato utilizzando <xref:System.Reflection.Emit?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="99fd1-112">The method returns `CORPROF_E_MODULE_IS_DYNAMIC` if the method was created using <xref:System.Reflection.Emit?displayProperty=nameWithType>.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="99fd1-113">Note</span><span class="sxs-lookup"><span data-stu-id="99fd1-113">Remarks</span></span>  
 <span data-ttu-id="99fd1-114">Se il modulo contiene i simboli in memoria, la lunghezza del flusso viene inserita nella `pCountSymbolBytes`.</span><span class="sxs-lookup"><span data-stu-id="99fd1-114">If the module has in-memory symbols, the length of the stream is placed in `pCountSymbolBytes`.</span></span> <span data-ttu-id="99fd1-115">Se il modulo privo di simboli in memoria, `*pCountSymbolBytes = 0`.</span><span class="sxs-lookup"><span data-stu-id="99fd1-115">If the module doesn't have in-memory     symbols, `*pCountSymbolBytes = 0`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="99fd1-116">L'implementazione corrente non supporta Reflection. Emit.</span><span class="sxs-lookup"><span data-stu-id="99fd1-116">The current implementation does not support Reflection.Emit.</span></span> <span data-ttu-id="99fd1-117">Se il modulo è stato creato tramite Reflection. Emit, il metodo restituisce `CORPROF_E_MODULE_IS_DYNAMIC`.</span><span class="sxs-lookup"><span data-stu-id="99fd1-117">If the module was created by using Reflection.Emit, the method returns `CORPROF_E_MODULE_IS_DYNAMIC`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99fd1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99fd1-118">Requirements</span></span>  
 <span data-ttu-id="99fd1-119">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="99fd1-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="99fd1-120">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="99fd1-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="99fd1-121">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="99fd1-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="99fd1-122">**Versioni di .NET Framework:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="99fd1-122">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99fd1-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="99fd1-123">See Also</span></span>  
 [<span data-ttu-id="99fd1-124">Interfaccia ICorProfilerInfo7</span><span class="sxs-lookup"><span data-stu-id="99fd1-124">ICorProfilerInfo7 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md)