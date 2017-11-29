---
title: Metodo ICorDebugNativeFrame::GetLocalRegisterValue
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugNativeFrame.GetLocalRegisterValue
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugNativeFrame::GetLocalRegisterValue
helpviewer_keywords:
- GetLocalRegisterValue method [.NET Framework debugging]
- ICorDebugNativeFrame::GetLocalRegisterValue method [.NET Framework debugging]
ms.assetid: 5ccb74f3-f891-430c-b70a-e370624edde2
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 43fdfc5cf4f17aaa9b26fc4a028c98c63a1b3c54
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugnativeframegetlocalregistervalue-method"></a><span data-ttu-id="b1c67-102">Metodo ICorDebugNativeFrame::GetLocalRegisterValue</span><span class="sxs-lookup"><span data-stu-id="b1c67-102">ICorDebugNativeFrame::GetLocalRegisterValue Method</span></span>
<span data-ttu-id="b1c67-103">Ottiene il valore di un argomento o una variabile locale viene archiviato nel registro specificato per il frame nativo.</span><span class="sxs-lookup"><span data-stu-id="b1c67-103">Gets the value of an argument or local variable that is stored in the specified register for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1c67-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1c67-104">Syntax</span></span>  
  
```  
HRESULT GetLocalRegisterValue (  
    [in]  CorDebugRegister   reg,  
    [in]  ULONG              cbSigBlob,  
    [in]  PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b1c67-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1c67-105">Parameters</span></span>  
 `reg`  
 <span data-ttu-id="b1c67-106">[in] Valore dell'enumerazione che specifica il registro contenente il valore "CorDebugRegister".</span><span class="sxs-lookup"><span data-stu-id="b1c67-106">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="b1c67-107">[in] Valore intero che specifica la dimensione della firma binaria dei metadati a cui fa riferimento il `pvSigBlob` parametro.</span><span class="sxs-lookup"><span data-stu-id="b1c67-107">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="b1c67-108">[in] Oggetto `PCCOR_SIGNATURE` che punta alla firma binaria dei metadati del tipo del valore.</span><span class="sxs-lookup"><span data-stu-id="b1c67-108">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="b1c67-109">[out] Un puntatore all'indirizzo di un oggetto "ICorDebugValue" che rappresenta il valore recuperato archiviato nel registro specificato.</span><span class="sxs-lookup"><span data-stu-id="b1c67-109">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b1c67-110">Note</span><span class="sxs-lookup"><span data-stu-id="b1c67-110">Remarks</span></span>  
 <span data-ttu-id="b1c67-111">Il `GetLocalRegisterValue` metodo può essere utilizzato in un frame nativo o un just-in-time (JIT)-frame compilato.</span><span class="sxs-lookup"><span data-stu-id="b1c67-111">The `GetLocalRegisterValue` method can be used either in a native frame or a just-in-time (JIT)-compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1c67-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1c67-112">Requirements</span></span>  
 <span data-ttu-id="b1c67-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1c67-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1c67-114">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="b1c67-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b1c67-115">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b1c67-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b1c67-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1c67-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1c67-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b1c67-117">See Also</span></span>  
 