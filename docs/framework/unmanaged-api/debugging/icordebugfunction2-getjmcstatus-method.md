---
title: Metodo ICorDebugFunction2::GetJMCStatus
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugFunction2.GetJMCStatus
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugFunction2::GetJMCStatus
helpviewer_keywords:
- ICorDebugFunction2::GetJMCStatus method [.NET Framework debugging]
- GetJMCStatus method [.NET Framework debugging]
ms.assetid: 840a71ed-bf5a-4f5e-8ed6-762222b34493
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: dc5e5e6a0ff0784825a69ba1873224a537ad46c3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugfunction2getjmcstatus-method"></a><span data-ttu-id="fcf2c-102">Metodo ICorDebugFunction2::GetJMCStatus</span><span class="sxs-lookup"><span data-stu-id="fcf2c-102">ICorDebugFunction2::GetJMCStatus Method</span></span>
<span data-ttu-id="fcf2c-103">Ottiene un valore che indica se la funzione che è rappresentata dall'oggetto ICorDebugFunction2 è contrassegnata come codice utente.</span><span class="sxs-lookup"><span data-stu-id="fcf2c-103">Gets a value that indicates whether the function that is represented by this ICorDebugFunction2 object is marked as user code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fcf2c-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fcf2c-104">Syntax</span></span>  
  
```  
HRESULT GetJMCStatus (  
    [out] BOOL   *pbIsJustMyCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fcf2c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcf2c-105">Parameters</span></span>  
 `pbIsJustMyCode`  
 <span data-ttu-id="fcf2c-106">[out] Un puntatore a un valore booleano che è `true`, se questa funzione è contrassegnata come codice utente; in caso contrario, il valore è `false`.</span><span class="sxs-lookup"><span data-stu-id="fcf2c-106">[out] A pointer to a Boolean value that is `true`, if this function is marked as user code; otherwise, the value is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fcf2c-107">Note</span><span class="sxs-lookup"><span data-stu-id="fcf2c-107">Remarks</span></span>  
 <span data-ttu-id="fcf2c-108">Se la funzione è rappresentato da questo `ICorDebugFunction2` Impossibile eseguire il debug, `pbIsJustMyCode` sarà sempre `false`.</span><span class="sxs-lookup"><span data-stu-id="fcf2c-108">If the function represented by this `ICorDebugFunction2` cannot be debugged, `pbIsJustMyCode` will always be `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fcf2c-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcf2c-109">Requirements</span></span>  
 <span data-ttu-id="fcf2c-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fcf2c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fcf2c-111">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="fcf2c-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fcf2c-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fcf2c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fcf2c-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fcf2c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>