---
title: Interfaccia ICorDebugSymbolProvider2
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 1c9c3d92-f0de-4d4d-87f1-0c702a4808af
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5ff0446ba8646620cb7322f74a81769e41f35b0d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugsymbolprovider2-interface"></a><span data-ttu-id="1fe0a-102">Interfaccia ICorDebugSymbolProvider2</span><span class="sxs-lookup"><span data-stu-id="1fe0a-102">ICorDebugSymbolProvider2 Interface</span></span>
<span data-ttu-id="1fe0a-103">Estende logicamente il [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) interfaccia per il recupero di informazioni sui simboli di debug aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="1fe0a-103">Logically extends the [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) interface to retrieve additional debug symbol information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1fe0a-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="1fe0a-104">Methods</span></span>  
  
|<span data-ttu-id="1fe0a-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="1fe0a-105">Method</span></span>|<span data-ttu-id="1fe0a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fe0a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1fe0a-107">Metodo GetFrameProps</span><span class="sxs-lookup"><span data-stu-id="1fe0a-107">GetFrameProps Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider2-getframeprops-method.md)|<span data-ttu-id="1fe0a-108">Restituisce l'indirizzo RVA (Relative Virtual Address) iniziale di un metodo e il frame padre in base a un indirizzo virtuale relativo al codice.</span><span class="sxs-lookup"><span data-stu-id="1fe0a-108">Returns the method starting relative virtual address of a method and the parent frame given a code relative virtual address.</span></span>|  
|[<span data-ttu-id="1fe0a-109">Metodo GetGenericDictionaryInfo</span><span class="sxs-lookup"><span data-stu-id="1fe0a-109">GetGenericDictionaryInfo Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider2-getgenericdictionaryinfo-method.md)|<span data-ttu-id="1fe0a-110">Recupera una mappa di dizionari generici.</span><span class="sxs-lookup"><span data-stu-id="1fe0a-110">Retrieves a generic dictionary map.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1fe0a-111">Note</span><span class="sxs-lookup"><span data-stu-id="1fe0a-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1fe0a-112">Questa interfaccia è disponibile solo con .NET Native.</span><span class="sxs-lookup"><span data-stu-id="1fe0a-112">This interface is available with .NET Native only.</span></span> <span data-ttu-id="1fe0a-113">Se questa interfaccia viene implementata per scenari ICorDebug al di fuori di .NET Native, sarà ignorata da Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="1fe0a-113">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fe0a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fe0a-114">Requirements</span></span>  
 <span data-ttu-id="1fe0a-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1fe0a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fe0a-116">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="1fe0a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1fe0a-117">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1fe0a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1fe0a-118">**Versioni di .NET framework:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fe0a-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fe0a-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1fe0a-119">See Also</span></span>  
 [<span data-ttu-id="1fe0a-120">Interfaccia ICorDebugSymbolProvider</span><span class="sxs-lookup"><span data-stu-id="1fe0a-120">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="1fe0a-121">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="1fe0a-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="1fe0a-122">Debug</span><span class="sxs-lookup"><span data-stu-id="1fe0a-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)