---
title: Metodo ICorDebugCode::GetCode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugCode.GetCode
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugCode::GetCode
helpviewer_keywords:
- ICorDebugCode::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 7137e3d1-1dad-48d8-8c37-16ac816534d3
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 12820d0be725c92754640aaa4eebca56bbc33ab6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugcodegetcode-method"></a><span data-ttu-id="ac806-102">Metodo ICorDebugCode::GetCode</span><span class="sxs-lookup"><span data-stu-id="ac806-102">ICorDebugCode::GetCode Method</span></span>
<span data-ttu-id="ac806-103">Ottiene il codice per la funzione specificata, formattata per il disassembly.</span><span class="sxs-lookup"><span data-stu-id="ac806-103">Gets all the code for the specified function, formatted for disassembly.</span></span> <span data-ttu-id="ac806-104">Questo metodo è obsoleto in .NET Framework versione 2.0.</span><span class="sxs-lookup"><span data-stu-id="ac806-104">This method has been deprecated in the .NET Framework version 2.0.</span></span> <span data-ttu-id="ac806-105">Utilizzare [ICorDebugCode2:: GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) invece.</span><span class="sxs-lookup"><span data-stu-id="ac806-105">Use [ICorDebugCode2::GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac806-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac806-106">Syntax</span></span>  
  
```  
HRESULT GetCode (  
    [in] ULONG32     startOffset,   
    [in] ULONG32     endOffset,  
    [in] ULONG32     cBufferAlloc,  
    [out, size_is(cBufferAlloc),  
        length_is(*pcBufferSize)] BYTE buffer[],  
    [out] ULONG32    *pcBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ac806-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac806-107">Parameters</span></span>  
 `startOffset`  
 <span data-ttu-id="ac806-108">[in] L'offset dell'inizio della funzione.</span><span class="sxs-lookup"><span data-stu-id="ac806-108">[in] The offset of the beginning of the function.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="ac806-109">[in] L'offset della fine della funzione.</span><span class="sxs-lookup"><span data-stu-id="ac806-109">[in] The offset of the end of the function.</span></span>  
  
 `cBufferAlloc`  
 <span data-ttu-id="ac806-110">[in] Le dimensioni del `buffer` della matrice in cui verrà restituito il codice.</span><span class="sxs-lookup"><span data-stu-id="ac806-110">[in] The size of the `buffer` array into which the code will be returned.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ac806-111">[out] Matrice in cui verrà restituito il codice.</span><span class="sxs-lookup"><span data-stu-id="ac806-111">[out] The array into which the code will be returned.</span></span>  
  
 `pcBufferSize`  
 <span data-ttu-id="ac806-112">[out] Il numero di byte restituiti.</span><span class="sxs-lookup"><span data-stu-id="ac806-112">[out] The number of bytes returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ac806-113">Note</span><span class="sxs-lookup"><span data-stu-id="ac806-113">Remarks</span></span>  
 <span data-ttu-id="ac806-114">Se il codice della funzione è stato suddiviso in più blocchi, questi vengono concatenati in ordine crescente di offset nativo.</span><span class="sxs-lookup"><span data-stu-id="ac806-114">If the function's code has been divided into multiple chunks, they are concatenated in order of increasing native offset.</span></span> <span data-ttu-id="ac806-115">Non vengono controllati i limiti di istruzione.</span><span class="sxs-lookup"><span data-stu-id="ac806-115">Instruction boundaries are not checked.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac806-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac806-116">Requirements</span></span>  
 <span data-ttu-id="ac806-117">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ac806-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac806-118">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="ac806-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ac806-119">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ac806-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ac806-120">**Versioni di .NET framework:** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="ac806-120">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac806-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ac806-121">See Also</span></span>  
 [<span data-ttu-id="ac806-122">GetCodeChunks (metodo)</span><span class="sxs-lookup"><span data-stu-id="ac806-122">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)  
 