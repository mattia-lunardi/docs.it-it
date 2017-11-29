---
title: Metodo ICorProfilerInfo::GetILFunctionBodyAllocator
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.GetILFunctionBodyAllocator
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::GetILFunctionBodyAllocator
helpviewer_keywords:
- GetILFunctionBodyAllocator method [.NET Framework profiling]
- ICorProfilerInfo::GetILFunctionBodyAllocator method [.NET Framework profiling]
ms.assetid: 5da1bf3d-dddf-4892-b266-578ee54d570b
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 45a50fc39f2df9d4998f8490ff4382c84c5aa9bb
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerinfogetilfunctionbodyallocator-method"></a><span data-ttu-id="b3189-102">Metodo ICorProfilerInfo::GetILFunctionBodyAllocator</span><span class="sxs-lookup"><span data-stu-id="b3189-102">ICorProfilerInfo::GetILFunctionBodyAllocator Method</span></span>
<span data-ttu-id="b3189-103">Ottiene un'interfaccia che fornisce un metodo per allocare memoria per essere utilizzato per scambiare il corpo di un metodo in codice Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="b3189-103">Gets an interface that provides a method to allocate memory to be used for swapping out the body of a method in Microsoft intermediate language (MSIL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3189-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3189-104">Syntax</span></span>  
  
```  
HRESULT GetILFunctionBodyAllocator(  
    [in]  ModuleID      moduleId,  
    [out] IMethodMalloc **ppMalloc);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b3189-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3189-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="b3189-106">[in] L'ID del modulo in cui risiede il metodo.</span><span class="sxs-lookup"><span data-stu-id="b3189-106">[in] The ID of the module in which the method resides.</span></span>  
  
 `ppMalloc`  
 <span data-ttu-id="b3189-107">[out] Un puntatore a un [IMethodMalloc](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md) interfaccia che fornisce un metodo per allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="b3189-107">[out] A pointer to an [IMethodMalloc](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md) interface that provides a method to allocate the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b3189-108">Note</span><span class="sxs-lookup"><span data-stu-id="b3189-108">Remarks</span></span>  
 <span data-ttu-id="b3189-109">Il corpo di un metodo in codice MSIL deve essere individuato come indirizzi virtuali relativi (RVA), rispetto al modulo caricato, che significa che segue il modulo all'interno di 4 GB.</span><span class="sxs-lookup"><span data-stu-id="b3189-109">A method body in MSIL code must be located as a relative virtual address (RVA), relative to the loaded module, which means that it follows the module within 4 GB.</span></span> <span data-ttu-id="b3189-110">Per renderne più semplice per uno strumento di scambiare il corpo di un metodo, il `GetILFunctionBodyAllocator` metodo assicura che la memoria viene allocata all'interno dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="b3189-110">To make it easier for a tool to swap out the body of a method, the `GetILFunctionBodyAllocator` method ensures that memory is allocated within that range.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3189-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3189-111">Requirements</span></span>  
 <span data-ttu-id="b3189-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b3189-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3189-113">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b3189-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b3189-114">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b3189-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b3189-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3189-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3189-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b3189-116">See Also</span></span>  
 [<span data-ttu-id="b3189-117">Interfaccia ICorProfilerInfo</span><span class="sxs-lookup"><span data-stu-id="b3189-117">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)