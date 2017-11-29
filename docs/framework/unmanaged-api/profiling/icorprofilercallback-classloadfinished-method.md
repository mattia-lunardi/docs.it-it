---
title: Metodo ICorProfilerCallback::ClassLoadFinished
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ClassLoadFinished
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ClassLoadFinished
helpviewer_keywords:
- ClassLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ClassLoadFinished method [.NET Framework profiling]
ms.assetid: 3dd80fbe-d62d-4d4d-acf8-5b7d0efe607e
topic_type: apiref
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: f3f321849c62ffd653ffa174ff91447a2c8eec73
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallbackclassloadfinished-method"></a><span data-ttu-id="44955-102">Metodo ICorProfilerCallback::ClassLoadFinished</span><span class="sxs-lookup"><span data-stu-id="44955-102">ICorProfilerCallback::ClassLoadFinished Method</span></span>
<span data-ttu-id="44955-103">Notifica al profiler che ha terminato il caricamento di una classe.</span><span class="sxs-lookup"><span data-stu-id="44955-103">Notifies the profiler that a class has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44955-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44955-104">Syntax</span></span>  
  
```  
HRESULT ClassLoadFinished(  
    [in] ClassID classId,  
    [in] HRESULT hrStatus);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="44955-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="44955-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="44955-106">[in] Identifica la classe che è stata caricata.</span><span class="sxs-lookup"><span data-stu-id="44955-106">[in] Identifies the class that was loaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="44955-107">[in] Un valore HRESULT che indica se la classe sia stato caricato correttamente.</span><span class="sxs-lookup"><span data-stu-id="44955-107">[in] An HRESULT that indicates whether the class loaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="44955-108">Note</span><span class="sxs-lookup"><span data-stu-id="44955-108">Remarks</span></span>  
 <span data-ttu-id="44955-109">Il valore di `classId` non è valido per una richiesta di informazioni fino a quando il `ClassLoadFinished` metodo viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="44955-109">The value of `classId` is not valid for an information request until the `ClassLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="44955-110">Alcune parti del caricamento della classe potrebbero continuare dopo il `ClassLoadFinished` callback.</span><span class="sxs-lookup"><span data-stu-id="44955-110">Some parts of loading the class might continue after the `ClassLoadFinished` callback.</span></span> <span data-ttu-id="44955-111">Un HRESULT di errore in `hrStatus` indica un errore.</span><span class="sxs-lookup"><span data-stu-id="44955-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="44955-112">Tuttavia, un HRESULT positivo in `hrStatus` indica solo che la prima parte del caricamento della classe ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="44955-112">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the class has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44955-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44955-113">Requirements</span></span>  
 <span data-ttu-id="44955-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="44955-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44955-115">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="44955-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="44955-116">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="44955-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="44955-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44955-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44955-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="44955-118">See Also</span></span>  
 [<span data-ttu-id="44955-119">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="44955-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="44955-120">ClassLoadStarted (metodo)</span><span class="sxs-lookup"><span data-stu-id="44955-120">ClassLoadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadstarted-method.md)