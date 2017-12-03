---
title: Funzione GetCORSystemDirectory
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetCORSystemDirectory
api_location:
- mscoree.dll
- mscoreei.dll
api_type: DLLExport
f1_keywords: GetCORSystemDirectory
helpviewer_keywords: GetCORSystemDirectory function [.NET Framework hosting]
ms.assetid: 3dcd16a7-dafc-4ca8-b5cd-20ffb37db91d
topic_type: apiref
caps.latest.revision: "21"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 802e9a7bd4e6caedd657a8e8cf0132d75b4cbc2e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="getcorsystemdirectory-function"></a><span data-ttu-id="90fbe-102">Funzione GetCORSystemDirectory</span><span class="sxs-lookup"><span data-stu-id="90fbe-102">GetCORSystemDirectory Function</span></span>
<span data-ttu-id="90fbe-103">Restituisce la directory di installazione di common language runtime (CLR) che viene caricato nel processo.</span><span class="sxs-lookup"><span data-stu-id="90fbe-103">Returns the installation directory of the common language runtime (CLR) that is loaded into the process.</span></span> <span data-ttu-id="90fbe-104">La directory di installazione è completo, ad esempio, "c:\windows\microsoft.net\framework\v1.0.3705".</span><span class="sxs-lookup"><span data-stu-id="90fbe-104">The installation directory is fully qualified, for example, "c:\windows\microsoft.net\framework\v1.0.3705".</span></span>  
  
 <span data-ttu-id="90fbe-105">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="90fbe-105">This function is deprecated.</span></span> <span data-ttu-id="90fbe-106">Viene sostituito dal [GetRuntimeDirectory](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getruntimedirectory-method.md) fornito nel metodo il [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="90fbe-106">It is superseded by the [ICLRRuntimeInfo::GetRuntimeDirectory](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getruntimedirectory-method.md) method provided in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90fbe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90fbe-107">Syntax</span></span>  
  
```  
HRESULT GetCORSystemDirectory (   
    [out] LPWSTR  pbuffer,     
    [in]  DWORD   cchBuffer,   
    [out] DWORD*  dwlength  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="90fbe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="90fbe-108">Parameters</span></span>  
 `pbuffer`  
 <span data-ttu-id="90fbe-109">[out] Un buffer in cui il runtime restituisce una stringa che contiene il nome completo della directory di installazione per il runtime che viene caricato nel processo.</span><span class="sxs-lookup"><span data-stu-id="90fbe-109">[out] A buffer in which the runtime returns a string that contains the fully qualified name of the installation directory for the runtime that is loaded into the process.</span></span> <span data-ttu-id="90fbe-110">Se il runtime non è ancora stato caricato nel processo, la funzione restituisce le informazioni di directory appropriata per la versione più recente del runtime installata nel computer.</span><span class="sxs-lookup"><span data-stu-id="90fbe-110">If the runtime has not yet been loaded into the process, the function returns the appropriate directory information for the latest version of the runtime installed on the computer.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="90fbe-111">[in] Le dimensioni, in byte, di `pbuffer`.</span><span class="sxs-lookup"><span data-stu-id="90fbe-111">[in] The size, in bytes, of `pbuffer`.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="90fbe-112">[out] Il numero di caratteri restituiti in `pbuffer`.</span><span class="sxs-lookup"><span data-stu-id="90fbe-112">[out] The number of characters returned in `pbuffer`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="90fbe-113">Note</span><span class="sxs-lookup"><span data-stu-id="90fbe-113">Remarks</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="90fbe-114">Non utilizzare questa funzione in processi che eseguono la versione 4 di CLR.</span><span class="sxs-lookup"><span data-stu-id="90fbe-114">Do not use this function in processes that are running version 4 of the CLR.</span></span> <span data-ttu-id="90fbe-115">Se una versione precedente di CLR è installata nel computer, questa funzione restituisce la directory di installazione per tale versione.</span><span class="sxs-lookup"><span data-stu-id="90fbe-115">If an earlier version of the CLR is installed on the computer, this function returns the installation directory for that version.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90fbe-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90fbe-116">Requirements</span></span>  
 <span data-ttu-id="90fbe-117">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="90fbe-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90fbe-118">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="90fbe-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="90fbe-119">**Libreria:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="90fbe-119">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="90fbe-120">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="90fbe-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90fbe-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="90fbe-121">See Also</span></span>  
 [<span data-ttu-id="90fbe-122">Funzioni di Hosting CLR deprecate</span><span class="sxs-lookup"><span data-stu-id="90fbe-122">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)