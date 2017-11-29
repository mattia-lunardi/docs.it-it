---
title: Metodo ICorDebugObjectValue::GetClass
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugObjectValue.GetClass
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugObjectValue::GetClass
helpviewer_keywords:
- ICorDebugObjectValue::GetClass method [.NET Framework debugging]
- GetClass method, ICorDebugObjectValue interface [.NET Framework debugging]
ms.assetid: 5be25292-8357-445f-a09b-f997c0de761c
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: dee9f110647230e54df527959651dc5b2fb73b3f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugobjectvaluegetclass-method"></a><span data-ttu-id="d9a64-102">Metodo ICorDebugObjectValue::GetClass</span><span class="sxs-lookup"><span data-stu-id="d9a64-102">ICorDebugObjectValue::GetClass Method</span></span>
<span data-ttu-id="d9a64-103">Ottiene la classe di valore di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d9a64-103">Gets the class of this object value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9a64-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9a64-104">Syntax</span></span>  
  
```  
HRESULT GetClass (  
    [out] ICorDebugClass     **ppClass  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d9a64-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9a64-105">Parameters</span></span>  
 `ppClass`  
 <span data-ttu-id="d9a64-106">[out] Un puntatore all'indirizzo di un oggetto "ICorDebugClass" che rappresenta la classe del valore dell'oggetto rappresentato dall'oggetto "ICorDebugObjectValue".</span><span class="sxs-lookup"><span data-stu-id="d9a64-106">[out] A pointer to the address of an "ICorDebugClass" object that represents the class of the object value represented by this "ICorDebugObjectValue" object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d9a64-107">Note</span><span class="sxs-lookup"><span data-stu-id="d9a64-107">Remarks</span></span>  
 <span data-ttu-id="d9a64-108">Il `GetClass` e [ICorDebugValue:: GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md) i metodi restituiscono informazioni sul tipo di valore; entrambi vengono sostituiti da GetExactType [Icordebugvalue2](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md).</span><span class="sxs-lookup"><span data-stu-id="d9a64-108">The `GetClass` and [ICorDebugValue::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md) methods each return information about the type of a value; they are both superseded by the generics-aware [ICorDebugValue2::GetExactType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9a64-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9a64-109">Requirements</span></span>  
 <span data-ttu-id="d9a64-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d9a64-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9a64-111">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="d9a64-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d9a64-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d9a64-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d9a64-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9a64-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9a64-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d9a64-114">See Also</span></span>  
    
 