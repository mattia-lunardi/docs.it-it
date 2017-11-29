---
title: Interfaccia IMethodMalloc
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMethodMalloc
api_location: mscorwks.dll
api_type: COM
f1_keywords: IMethodMalloc
helpviewer_keywords: IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8c8ab5dc-557c-473a-82f2-6e403eca7dac
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: d246f329f80a76d2c93190fd663c7362418385f7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="imethodmalloc-interface"></a><span data-ttu-id="ec782-102">Interfaccia IMethodMalloc</span><span class="sxs-lookup"><span data-stu-id="ec782-102">IMethodMalloc Interface</span></span>
<span data-ttu-id="ec782-103">Fornisce un metodo per allocare memoria per un nuovo corpo della funzione Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="ec782-103">Provides a method to allocate memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ec782-104">Il `IMethodMalloc` interfaccia è un semplice allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="ec782-104">The `IMethodMalloc` interface is a simple memory allocator.</span></span> <span data-ttu-id="ec782-105">Consente di allocare memoria, ma non per liberarlo.</span><span class="sxs-lookup"><span data-stu-id="ec782-105">It allows you to allocate memory, but not to free it.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ec782-106">Metodi</span><span class="sxs-lookup"><span data-stu-id="ec782-106">Methods</span></span>  
  
|<span data-ttu-id="ec782-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="ec782-107">Method</span></span>|<span data-ttu-id="ec782-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec782-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ec782-109">Alloc (metodo)</span><span class="sxs-lookup"><span data-stu-id="ec782-109">Alloc Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-alloc-method.md)|<span data-ttu-id="ec782-110">Tenta di allocare una quantità di memoria specificata per il corpo di una nuova funzione MSIL.</span><span class="sxs-lookup"><span data-stu-id="ec782-110">Attempts to allocate a specified amount of memory for a new MSIL function body.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ec782-111">Note</span><span class="sxs-lookup"><span data-stu-id="ec782-111">Remarks</span></span>  
 <span data-ttu-id="ec782-112">Ogni allocatore è specifico del modulo e assicura che il corpo della funzione sarà un offset positivo dalla base del modulo.</span><span class="sxs-lookup"><span data-stu-id="ec782-112">Each allocator is module-specific and ensures that the function body will be at a positive offset from the base of the module.</span></span> <span data-ttu-id="ec782-113">Memoria di sopra della base di un modulo può essere preziosa, pertanto l'allocatore deve essere utilizzata per allocare memoria solo per un corpo della funzione.</span><span class="sxs-lookup"><span data-stu-id="ec782-113">Memory above the base of a module can be precious, so the allocator should be used to allocate memory only for a function body.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec782-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec782-114">Requirements</span></span>  
 <span data-ttu-id="ec782-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec782-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec782-116">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ec782-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ec782-117">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ec782-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ec782-118">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec782-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec782-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ec782-119">See Also</span></span>  
 [<span data-ttu-id="ec782-120">Interfacce di profilatura</span><span class="sxs-lookup"><span data-stu-id="ec782-120">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)