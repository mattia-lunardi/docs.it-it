---
title: Funzione StrongNameErrorInfo
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StrongNameErrorInfo
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type: DLLExport
f1_keywords: StrongNameErrorInfo
helpviewer_keywords: StrongNameErrorInfo function [.NET Framework strong naming]
ms.assetid: e91bf8c3-7c26-4732-938e-2e5b04abfc99
topic_type: apiref
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0fbe77f16ed022458a036b6627b82f80d194276c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="strongnameerrorinfo-function"></a><span data-ttu-id="e9e99-102">Funzione StrongNameErrorInfo</span><span class="sxs-lookup"><span data-stu-id="e9e99-102">StrongNameErrorInfo Function</span></span>
<span data-ttu-id="e9e99-103">Ottiene l'ultimo codice di errore che è stato generato da una delle funzioni con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="e9e99-103">Gets the last error code that was raised by one of the strong name functions.</span></span>  
  
 <span data-ttu-id="e9e99-104">Questa funzione è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="e9e99-104">This function has been deprecated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9e99-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9e99-105">Syntax</span></span>  
  
```  
HRESULT StrongNameErrorInfo ();   
```  
  
## <a name="return-value"></a><span data-ttu-id="e9e99-106">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9e99-106">Return Value</span></span>  
 <span data-ttu-id="e9e99-107">L'ultimo codice di errore COM impostato da una delle funzioni con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="e9e99-107">The last COM error code set by one of the strong name functions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e9e99-108">Note</span><span class="sxs-lookup"><span data-stu-id="e9e99-108">Remarks</span></span>  
 <span data-ttu-id="e9e99-109">La maggior parte dei metodi con nome sicuro restituisce una semplice `true` o `false` indicazione del completamento.</span><span class="sxs-lookup"><span data-stu-id="e9e99-109">Most of the strong name methods return a simple `true` or `false` indication of successful completion.</span></span> <span data-ttu-id="e9e99-110">Utilizzare il `StrongNameErrorInfo` funzione per recuperare un valore HRESULT che specifica l'ultimo errore generato dalle funzioni con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="e9e99-110">Use the `StrongNameErrorInfo` function to retrieve an HRESULT that specifies the last error generated by the strong name functions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e9e99-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9e99-111">Requirements</span></span>  
 <span data-ttu-id="e9e99-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e9e99-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e9e99-113">**Intestazione:** StrongName. H</span><span class="sxs-lookup"><span data-stu-id="e9e99-113">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="e9e99-114">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e9e99-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e9e99-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e9e99-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9e99-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e9e99-116">See Also</span></span>  
 [<span data-ttu-id="e9e99-117">Funzioni statiche globali di denominazione sicura</span><span class="sxs-lookup"><span data-stu-id="e9e99-117">Strong Naming Global Static Functions</span></span>](http://msdn.microsoft.com/en-us/efa715df-e8cc-48f2-9ec4-26586f0dc8d0)