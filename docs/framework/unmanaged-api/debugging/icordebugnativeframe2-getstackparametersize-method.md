---
title: Metodo ICorDebugNativeFrame2::GetStackParameterSize
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugNativeFrame2.GetStackParameterSize Method
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugNativeFrame2::GetStackParameterSize
helpviewer_keywords:
- ICorDebugNativeFrame2::GetStackParameterSize method [.NET Framework debugging]
- GetStackParameterSize method [.NET Framework debugging]
ms.assetid: f6a449c8-a941-43ba-9a90-c98b29ae3c36
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c265cb564718b362b1354189e59dc217b2866b36
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugnativeframe2getstackparametersize-method"></a><span data-ttu-id="1eab8-102">Metodo ICorDebugNativeFrame2::GetStackParameterSize</span><span class="sxs-lookup"><span data-stu-id="1eab8-102">ICorDebugNativeFrame2::GetStackParameterSize Method</span></span>
<span data-ttu-id="1eab8-103">Restituisce la dimensione complessiva dei parametri nello stack su sistemi operativi x86.</span><span class="sxs-lookup"><span data-stu-id="1eab8-103">Returns the cumulative size of the parameters on the stack on x86 operating systems.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1eab8-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1eab8-104">Syntax</span></span>  
  
```  
HRESULT GetStackParameterSize([out] ULONG32 * pSize)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1eab8-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1eab8-105">Parameters</span></span>  
 `pSize`  
 <span data-ttu-id="1eab8-106">[out] Un puntatore per la dimensione complessiva dei parametri nello stack.</span><span class="sxs-lookup"><span data-stu-id="1eab8-106">[out] A pointer to the cumulative size of the parameters on the stack.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1eab8-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1eab8-107">Return Value</span></span>  
 <span data-ttu-id="1eab8-108">Questo metodo restituisce gli specifici HRESULT seguenti, nonché gli errori di HRESULT che indicano la mancata riuscita del metodo.</span><span class="sxs-lookup"><span data-stu-id="1eab8-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="1eab8-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1eab8-109">HRESULT</span></span>|<span data-ttu-id="1eab8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1eab8-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1eab8-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1eab8-111">S_OK</span></span>|<span data-ttu-id="1eab8-112">La dimensione dello stack è stata restituita correttamente.</span><span class="sxs-lookup"><span data-stu-id="1eab8-112">The stack size was successfully returned.</span></span>|  
|<span data-ttu-id="1eab8-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1eab8-113">S_FALSE</span></span>|<span data-ttu-id="1eab8-114">`GetStackParameterSize`è stato chiamato su una piattaforma non x86.</span><span class="sxs-lookup"><span data-stu-id="1eab8-114">`GetStackParameterSize` was called on a non-x86 platform.</span></span>|  
|<span data-ttu-id="1eab8-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1eab8-115">E_FAIL</span></span>|<span data-ttu-id="1eab8-116">`The size of the parameters could not be returned`.</span><span class="sxs-lookup"><span data-stu-id="1eab8-116">`The size of the parameters could not be returned`.</span></span>|  
|<span data-ttu-id="1eab8-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1eab8-117">E_INVALIDARG</span></span>|<span data-ttu-id="1eab8-118">`pSize`È `null`.</span><span class="sxs-lookup"><span data-stu-id="1eab8-118">`pSize` Is `null`.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="1eab8-119">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="1eab8-119">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1eab8-120">Note</span><span class="sxs-lookup"><span data-stu-id="1eab8-120">Remarks</span></span>  
 <span data-ttu-id="1eab8-121">Il [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) metodi non regolano il puntatore dello stack per i parametri che vengono inseriti nello stack.</span><span class="sxs-lookup"><span data-stu-id="1eab8-121">The [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) methods do not adjust the stack pointer for parameters that are pushed on the stack.</span></span> <span data-ttu-id="1eab8-122">In alternativa, è possibile utilizzare il valore restituito da `GetStackParameterSize` per regolare il puntatore dello stack per l'inizializzazione di un agente di rimozione nativo, viene regolato per i parametri.</span><span class="sxs-lookup"><span data-stu-id="1eab8-122">Instead, you can use the value returned by `GetStackParameterSize` to adjust the stack pointer to seed a native unwinder, which does adjust for the parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1eab8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1eab8-123">Requirements</span></span>  
 <span data-ttu-id="1eab8-124">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1eab8-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1eab8-125">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="1eab8-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1eab8-126">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1eab8-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1eab8-127">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1eab8-127">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1eab8-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1eab8-128">See Also</span></span>  
 [<span data-ttu-id="1eab8-129">ICorDebugNativeFrame2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="1eab8-129">ICorDebugNativeFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-interface.md)  
 [<span data-ttu-id="1eab8-130">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="1eab8-130">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="1eab8-131">Debug</span><span class="sxs-lookup"><span data-stu-id="1eab8-131">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)