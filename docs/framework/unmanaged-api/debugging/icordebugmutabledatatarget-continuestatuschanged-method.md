---
title: Metodo ICorDebugMutableDataTarget::ContinueStatusChanged
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 5a66d3f4-dd16-4d62-9dcc-0eab7041d894
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2f4f3890f2cfb2e3b017b8c7d0705d8c8e063957
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmutabledatatargetcontinuestatuschanged-method"></a><span data-ttu-id="00d4b-102">Metodo ICorDebugMutableDataTarget::ContinueStatusChanged</span><span class="sxs-lookup"><span data-stu-id="00d4b-102">ICorDebugMutableDataTarget::ContinueStatusChanged Method</span></span>
<span data-ttu-id="00d4b-103">Modifica lo stato di continuazione per l'evento di debug in sospeso sul thread specificato.</span><span class="sxs-lookup"><span data-stu-id="00d4b-103">Changes the continuation status for the outstanding debug event on the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00d4b-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00d4b-104">Syntax</span></span>  
  
```  
HRESULT ContinueStatusChanged(  
   [in] DWORD dwThreadId,  
   [in] CORDB_CONTINUE_STATUS continueStatus);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="00d4b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="00d4b-105">Parameters</span></span>  
 `dwThreadId`  
 <span data-ttu-id="00d4b-106">Identificatore del thread definito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="00d4b-106">The operating system-defined thread identifier.</span></span>  
  
 `continueStatus`  
 <span data-ttu-id="00d4b-107">Oggetto[COREDB_CONTINUE_STATUS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)valore che rappresenta il nuovo stato di continuazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="00d4b-107">A[COREDB_CONTINUE_STATUS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)value that represents the new requested continuation status.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="00d4b-108">Note</span><span class="sxs-lookup"><span data-stu-id="00d4b-108">Remarks</span></span>  
 <span data-ttu-id="00d4b-109">Il debugger chiama il metodo `ContinueStatusChanged` quando chiama un metodo ICorDebug che richiede di gestire l'evento di debug corrente in modo potenzialmente diverso da quello in cui verrebbe gestito di solito.</span><span class="sxs-lookup"><span data-stu-id="00d4b-109">The debugger calls the `ContinueStatusChanged` method when it calls an ICorDebug method that requires the current debug event to be handled in a way that is potentially different from the way in which it normally would be handled.</span></span> <span data-ttu-id="00d4b-110">Ad esempio, se si verifica un'eccezione in sospeso e il debugger richiede un'operazione che annullerebbe l'accezione (ad esempio [ICorDebugILFrame:: SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md) o `FuncEval`), questa API viene usata per richiedere che l'eccezione venga annullata.</span><span class="sxs-lookup"><span data-stu-id="00d4b-110">For example, if there is an outstanding exception, and the debugger requests an operation that would cancel the exception (such as [ICorDebugILFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md) or `FuncEval`), this API is used to request that the exception be cancelled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00d4b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00d4b-111">Requirements</span></span>  
 <span data-ttu-id="00d4b-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="00d4b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00d4b-113">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="00d4b-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="00d4b-114">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="00d4b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="00d4b-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00d4b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00d4b-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="00d4b-116">See Also</span></span>  
 [<span data-ttu-id="00d4b-117">Interfaccia ICorDebugMutableDataTarget</span><span class="sxs-lookup"><span data-stu-id="00d4b-117">ICorDebugMutableDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)  
 [<span data-ttu-id="00d4b-118">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="00d4b-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)